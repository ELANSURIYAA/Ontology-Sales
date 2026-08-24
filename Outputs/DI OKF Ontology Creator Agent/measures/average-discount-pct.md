---
title: Average Discount Percentage
type: measure
description: Average discount applied to booked items or services, stored as a fractional percentage
resource: measures
tags: [discount, pricing, metric, percentage]
timestamp: 2026-07-28T00:00:00Z
---

# Average Discount Percentage

## Business Definition

Average Discount Percentage represents the average discount applied to booked items or services, stored as a fractional percentage of list price. This measure provides insight into pricing strategies, discount trends, and pricing effectiveness across all dimensions.

---

## Formula

**Expression**: AVG(bookings.discount_pct)

**Dialect**: ANSI_SQL

**Aggregation Type**: AVG

---

## Business Purpose

This measure enables:

- **Pricing Strategy Analysis**: Monitor discount trends and pricing effectiveness
- **Margin Management**: Track discount impact on profit margins
- **Competitive Analysis**: Compare discount levels across segments and products
- **Sales Behavior**: Analyze sales representative discount patterns
- **Channel Analysis**: Evaluate discount levels by partner and route to market
- **Negotiation Insights**: Understand discount patterns by customer segment and deal size

---

## Related Entities

**Primary Entity**: [Bookings](../entities/bookings.md)

**Dimensional Analysis**: This measure can be analyzed across all dimension entities:
- [Customers](../entities/customers.md) - Discount by customer segment, industry, account tier
- [Products](../entities/products.md) - Discount by product family, technology domain, offer type
- [Partners](../entities/partners.md) - Discount by partner type, tier, route to market
- [Geographies](../entities/geographies.md) - Discount by region, theater, country
- [Sales Representatives](../entities/sales-representatives.md) - Discount by sales role, team, segment
- [Contracts](../entities/contracts.md) - Discount by contract type, term, coverage level
- [Dates](../entities/dates.md) - Discount by fiscal year, quarter, month

---

## Related Concepts

- [Discount Percentage](../glossary/discount-percentage.md)
- [Booking Amount](../glossary/booking-amount.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Calculation Logic

The measure calculates the average of the discount_pct field from all booking records. The discount percentage is stored as a fractional value where:
- 0.00 = 0% discount (no discount)
- 0.15 = 15% discount
- 0.25 = 25% discount

The booking amount is calculated as:
```
booking_amount_usd = quantity × unit_list_price_usd × (1 - discount_pct)
```

---

## Usage Examples

### Average Discount by Fiscal Quarter
```sql
SELECT 
    dates.fiscal_year,
    dates.fiscal_quarter,
    AVG(bookings.discount_pct) as avg_discount_pct
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.fiscal_year, dates.fiscal_quarter
```

### Average Discount by Product Family
```sql
SELECT 
    products.product_family,
    AVG(bookings.discount_pct) as avg_discount_pct
FROM bookings
JOIN products ON bookings.product_key = products.product_key
GROUP BY products.product_family
ORDER BY avg_discount_pct DESC
```

---

## Business Rules

1. **Fractional Representation**: Discount is stored as a decimal between 0 and 1
2. **Valid Range**: Discount percentage must be between 0 (no discount) and 1 (100% discount)
3. **Average Calculation**: Simple average across all booking transactions
4. **Display Format**: Typically displayed as percentage (multiply by 100 for reporting)

---

## Related Measures

- [Total Booking Amount USD](./total-booking-amount-usd.md) - Net revenue after discounts
- [Average Selling Price USD](./average-selling-price-usd.md) - Average price per unit after discounts
- [Total Quantity](./total-quantity.md) - Total units sold

---

## Derived Metrics

### Weighted Average Discount
```
SUM(discount_pct × booking_amount_usd) / SUM(booking_amount_usd)
```

### Discount Impact on Revenue
```
SUM(quantity × unit_list_price_usd × discount_pct)
```

---

## Data Quality Considerations

- Ensure discount_pct is between 0 and 1
- Verify discount_pct is not null (use 0 for no discount)
- Confirm discount calculation is consistent with booking amount
- Validate discount levels are within approved ranges

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
