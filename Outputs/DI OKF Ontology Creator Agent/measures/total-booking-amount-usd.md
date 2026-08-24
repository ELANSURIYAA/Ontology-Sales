---
title: Total Booking Amount USD
type: measure
description: Total booked sales amount in US dollars after pricing and discount adjustments
resource: measures
tags: [booking-amount, revenue, metric, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Total Booking Amount USD

## Business Definition

Total Booking Amount USD represents the total booked sales amount in US dollars after pricing and discount adjustments. This is the primary revenue metric for the sales bookings and revenue analytics model, representing the total value of all completed booking transactions.

---

## Formula

**Expression**: SUM(bookings.booking_amount_usd)

**Dialect**: ANSI_SQL

**Aggregation Type**: SUM

---

## Business Purpose

This measure enables:

- **Revenue Tracking**: Monitor total booked revenue across all dimensions
- **Performance Analysis**: Evaluate sales performance against targets and quotas
- **Trend Analysis**: Track revenue trends over time
- **Segment Analysis**: Compare revenue across customer segments, products, and geographies
- **Financial Reporting**: Support financial reporting and forecasting
- **Commission Calculation**: Provide basis for sales commission calculations

---

## Related Entities

**Primary Entity**: [Bookings](../entities/bookings.md)

**Dimensional Analysis**: This measure can be analyzed across all dimension entities:
- [Customers](../entities/customers.md) - Revenue by customer segment, industry, account tier
- [Products](../entities/products.md) - Revenue by product family, technology domain, offer type
- [Partners](../entities/partners.md) - Revenue by partner type, tier, route to market
- [Geographies](../entities/geographies.md) - Revenue by region, theater, country
- [Sales Representatives](../entities/sales-representatives.md) - Revenue by sales role, team, segment
- [Contracts](../entities/contracts.md) - Revenue by contract type, term, coverage level
- [Dates](../entities/dates.md) - Revenue by fiscal year, quarter, month

---

## Related Concepts

- [Booking Amount](../glossary/booking-amount.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Calculation Logic

The measure sums the booking_amount_usd field from all booking records. The booking amount represents the net revenue after applying discounts to the list price multiplied by quantity:

```
booking_amount_usd = quantity × unit_list_price_usd × (1 - discount_pct)
```

---

## Usage Examples

### Fiscal Year Revenue
```sql
SELECT 
    dates.fiscal_year,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.fiscal_year
```

### Revenue by Customer Segment
```sql
SELECT 
    customers.segment,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN customers ON bookings.customer_key = customers.customer_key
GROUP BY customers.segment
ORDER BY total_booking_amount DESC
```

---

## Business Rules

1. **Non-Negative Values**: Booking amount must be non-negative
2. **Currency**: All amounts are in US dollars
3. **Net Amount**: Amount reflects net revenue after discounts
4. **Additive Measure**: Amounts can be summed across all dimensions

---

## Related Measures

- [Booking Count](./booking-count.md) - Count of booking transactions
- [Total Quantity](./total-quantity.md) - Total units booked
- [Total ACV USD](./total-acv-usd.md) - Total annual contract value
- [Total TCV USD](./total-tcv-usd.md) - Total contract value
- [Renewal Booking Amount USD](./renewal-booking-amount-usd.md) - Renewal revenue component
- [Net New Booking Amount USD](./net-new-booking-amount-usd.md) - Net new revenue component
- [Average Booking Value USD](./average-booking-value-usd.md) - Average value per booking
- [Average Selling Price USD](./average-selling-price-usd.md) - Average price per unit

---

## Derived Metrics

### Revenue Decomposition
```
Total Booking Amount USD = Renewal Booking Amount USD + Net New Booking Amount USD
```

### Average Booking Value
```
Total Booking Amount USD / Booking Count
```

### Average Selling Price
```
Total Booking Amount USD / Total Quantity
```

---

## Data Quality Considerations

- Ensure booking_amount_usd is non-negative and not null
- Verify booking amount calculation matches quantity × unit price × (1 - discount)
- Confirm currency conversion is applied consistently
- Validate booking amounts are within reasonable ranges

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
