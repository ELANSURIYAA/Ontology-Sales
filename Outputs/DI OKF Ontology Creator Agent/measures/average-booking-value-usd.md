---
title: Average Booking Value USD
type: measure
description: Average booking value in US dollars per distinct booking transaction
resource: measures
tags: [booking-value, average, metric, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Average Booking Value USD

## Business Definition

Average Booking Value USD represents the average booking value in US dollars per distinct booking transaction. This measure calculates the average deal size by dividing total booking amount by the number of booking transactions, providing insight into transaction size and deal value patterns.

---

## Formula

**Expression**: SUM(bookings.booking_amount_usd) / NULLIF(COUNT(DISTINCT bookings.booking_id), 0)

**Dialect**: ANSI_SQL

**Aggregation Type**: Calculated (Division)

---

## Business Purpose

This measure enables:

- **Deal Size Analysis**: Track average transaction values
- **Sales Performance**: Evaluate sales effectiveness by deal size
- **Trend Analysis**: Monitor changes in average deal size over time
- **Segment Analysis**: Compare average deal sizes across customer segments
- **Pricing Strategy**: Support pricing and packaging decisions
- **Sales Targeting**: Identify opportunities for deal size optimization

---

## Related Entities

**Primary Entity**: [Bookings](../entities/bookings.md)

**Dimensional Analysis**: This measure can be analyzed across all dimension entities:
- [Customers](../entities/customers.md) - Average booking value by customer segment, industry, account tier
- [Products](../entities/products.md) - Average booking value by product family, technology domain, offer type
- [Partners](../entities/partners.md) - Average booking value by partner type, tier, route to market
- [Geographies](../entities/geographies.md) - Average booking value by region, theater, country
- [Sales Representatives](../entities/sales-representatives.md) - Average booking value by sales role, team
- [Contracts](../entities/contracts.md) - Average booking value by contract type, term, coverage level
- [Dates](../entities/dates.md) - Average booking value by fiscal year, quarter, month

---

## Related Concepts

- [Booking Amount](../glossary/booking-amount.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Calculation Logic

The measure divides the total booking amount by the count of distinct booking transactions:

```
Average Booking Value = Total Booking Amount USD / Booking Count
```

The NULLIF function prevents division by zero errors when booking count is zero.

---

## Usage Examples

### Average Booking Value by Customer Segment
```sql
SELECT 
    customers.segment,
    SUM(bookings.booking_amount_usd) / NULLIF(COUNT(DISTINCT bookings.booking_id), 0) as avg_booking_value
FROM bookings
JOIN customers ON bookings.customer_key = customers.customer_key
GROUP BY customers.segment
```

### Average Booking Value Trend
```sql
SELECT 
    dates.fiscal_year,
    dates.fiscal_quarter,
    SUM(bookings.booking_amount_usd) / NULLIF(COUNT(DISTINCT bookings.booking_id), 0) as avg_booking_value
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.fiscal_year, dates.fiscal_quarter
```

---

## Business Rules

1. **Division by Zero Protection**: NULLIF prevents errors when booking count is zero
2. **Transaction Level**: Calculated at the booking transaction level
3. **Currency**: All amounts are in US dollars
4. **Distinct Count**: Uses distinct booking_id to ensure each transaction is counted once

---

## Related Measures

- [Total Booking Amount USD](./total-booking-amount-usd.md) - Total revenue (numerator)
- [Booking Count](./booking-count.md) - Count of transactions (denominator)
- [Average Selling Price USD](./average-selling-price-usd.md) - Average price per unit
- [Total Quantity](./total-quantity.md) - Total units sold

---

## Derived Metrics

### Deal Size Distribution
Analyze the distribution of booking values to understand deal size patterns

### Average Booking Value Growth
```
(Current Period Avg Booking Value - Prior Period Avg Booking Value) / Prior Period Avg Booking Value
```

---

## Data Quality Considerations

- Ensure booking_amount_usd is non-negative and not null
- Verify booking_id is unique and not null
- Confirm all booking transactions are captured
- Validate average booking values are within reasonable ranges

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
