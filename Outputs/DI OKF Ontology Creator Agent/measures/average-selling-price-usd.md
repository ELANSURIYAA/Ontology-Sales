---
title: Average Selling Price USD
type: measure
description: Average booked revenue per unit sold in US dollars
resource: measures
tags: [selling-price, pricing, metric, average, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Average Selling Price USD

## Business Definition

Average Selling Price USD represents the average booked revenue per unit sold in US dollars. This measure calculates the effective selling price per unit after discounts and pricing adjustments, providing insight into realized pricing and revenue per unit.

---

## Formula

**Expression**: SUM(bookings.booking_amount_usd) / NULLIF(SUM(bookings.quantity), 0)

**Dialect**: ANSI_SQL

**Aggregation Type**: Calculated (Division)

---

## Business Purpose

This measure enables:

- **Pricing Analysis**: Track effective selling prices after discounts
- **Price Realization**: Monitor actual prices achieved vs. list prices
- **Pricing Trends**: Analyze selling price trends over time
- **Product Pricing**: Compare selling prices across products and families
- **Segment Pricing**: Evaluate pricing by customer segment and geography
- **Margin Analysis**: Support gross margin and profitability analysis

---

## Related Entities

**Primary Entity**: [Bookings](../entities/bookings.md)

**Dimensional Analysis**: This measure can be analyzed across all dimension entities:
- [Customers](../entities/customers.md) - Selling price by customer segment, industry, account tier
- [Products](../entities/products.md) - Selling price by product family, technology domain, offer type
- [Partners](../entities/partners.md) - Selling price by partner type, tier, route to market
- [Geographies](../entities/geographies.md) - Selling price by region, theater, country
- [Sales Representatives](../entities/sales-representatives.md) - Selling price by sales role, team
- [Contracts](../entities/contracts.md) - Selling price by contract type, term
- [Dates](../entities/dates.md) - Selling price by fiscal year, quarter, month

---

## Related Concepts

- [Booking Amount](../glossary/booking-amount.md)
- [Discount Percentage](../glossary/discount-percentage.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Calculation Logic

The measure divides the total booking amount by the total quantity sold:

```
Average Selling Price = Total Booking Amount USD / Total Quantity
```

The NULLIF function prevents division by zero errors when quantity is zero.

The selling price reflects the net price after discounts:
```
Selling Price per Unit = unit_list_price_usd × (1 - discount_pct)
```

---

## Usage Examples

### Average Selling Price by Product Family
```sql
SELECT 
    products.product_family,
    SUM(bookings.booking_amount_usd) / NULLIF(SUM(bookings.quantity), 0) as avg_selling_price
FROM bookings
JOIN products ON bookings.product_key = products.product_key
GROUP BY products.product_family
```

### Selling Price Trend Over Time
```sql
SELECT 
    dates.fiscal_year,
    dates.fiscal_quarter,
    SUM(bookings.booking_amount_usd) / NULLIF(SUM(bookings.quantity), 0) as avg_selling_price
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.fiscal_year, dates.fiscal_quarter
```

---

## Business Rules

1. **Division by Zero Protection**: NULLIF prevents errors when quantity is zero
2. **Net Price**: Reflects actual selling price after discounts
3. **Currency**: All amounts are in US dollars
4. **Unit Consistency**: Assumes consistent unit definitions within aggregation context

---

## Related Measures

- [Total Booking Amount USD](./total-booking-amount-usd.md) - Total revenue (numerator)
- [Total Quantity](./total-quantity.md) - Total units sold (denominator)
- [Average Discount Percentage](./average-discount-pct.md) - Average discount applied
- [Average Booking Value USD](./average-booking-value-usd.md) - Average value per transaction

---

## Derived Metrics

### Price Realization Rate
```
Average Selling Price USD / Average List Price USD
```

### Discount Impact per Unit
```
Average List Price USD - Average Selling Price USD
```

---

## Data Quality Considerations

- Ensure booking_amount_usd is non-negative and not null
- Verify quantity is positive and not null
- Confirm unit definitions are consistent within product categories
- Validate selling prices are within reasonable ranges

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
