---
title: Net New Booking Amount USD
type: measure
description: Total booked sales amount in US dollars for non-renewal transactions
resource: measures
tags: [net-new, revenue, metric, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Net New Booking Amount USD

## Business Definition

Net New Booking Amount USD represents the total booked sales amount in US dollars for non-renewal transactions. This measure isolates revenue from new customer acquisition and expansion, providing insight into business growth and new customer revenue performance.

---

## Formula

**Expression**: SUM(CASE WHEN bookings.is_renewal = 0 THEN bookings.booking_amount_usd ELSE 0 END)

**Dialect**: ANSI_SQL

**Aggregation Type**: Conditional SUM

---

## Business Purpose

This measure enables:

- **Growth Analysis**: Track revenue from new customer acquisition
- **New Business Tracking**: Monitor new customer and expansion revenue
- **Sales Effectiveness**: Evaluate new business sales performance
- **Revenue Mix**: Understand the balance between new and renewal business
- **Market Expansion**: Measure success of market expansion strategies
- **Forecasting**: Project future new business revenue based on historical patterns

---

## Related Entities

**Primary Entity**: [Bookings](../entities/bookings.md)

**Dimensional Analysis**: This measure can be analyzed across all dimension entities:
- [Customers](../entities/customers.md) - Net new revenue by customer segment, industry, account tier
- [Products](../entities/products.md) - Net new revenue by product family, technology domain, offer type
- [Partners](../entities/partners.md) - Net new revenue by partner type, tier, route to market
- [Geographies](../entities/geographies.md) - Net new revenue by region, theater, country
- [Sales Representatives](../entities/sales-representatives.md) - Net new revenue by sales role, team
- [Contracts](../entities/contracts.md) - Net new revenue by contract type, term, coverage level
- [Dates](../entities/dates.md) - Net new revenue by fiscal year, quarter, month

---

## Related Concepts

- [Net New Business](../glossary/net-new-business.md)
- [Booking Amount](../glossary/booking-amount.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Calculation Logic

The measure sums the booking_amount_usd field only for records where is_renewal equals 0:

```
Net New Booking Amount = SUM(booking_amount_usd WHERE is_renewal = 0)
```

The is_renewal flag indicates whether a booking transaction represents a renewal (1) or net new business (0).

---

## Usage Examples

### Net New Revenue by Fiscal Year
```sql
SELECT 
    dates.fiscal_year,
    SUM(CASE WHEN bookings.is_renewal = 0 THEN bookings.booking_amount_usd ELSE 0 END) as net_new_amount
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.fiscal_year
```

### Net New Revenue by Product Family
```sql
SELECT 
    products.product_family,
    SUM(CASE WHEN bookings.is_renewal = 0 THEN bookings.booking_amount_usd ELSE 0 END) as net_new_amount
FROM bookings
JOIN products ON bookings.product_key = products.product_key
GROUP BY products.product_family
```

---

## Business Rules

1. **Non-Renewal Flag**: Only bookings with is_renewal = 0 are included
2. **Non-Negative Values**: Net new amounts must be non-negative
3. **Currency**: All amounts are in US dollars
4. **Additive Measure**: Amounts can be summed across all dimensions
5. **Mutually Exclusive**: A booking is either renewal or net new, not both

---

## Related Measures

- [Renewal Booking Amount USD](./renewal-booking-amount-usd.md) - Complementary measure for renewal business
- [Total Booking Amount USD](./total-booking-amount-usd.md) - Total revenue (renewal + net new)
- [Total ACV USD](./total-acv-usd.md) - Annual contract value
- [Total TCV USD](./total-tcv-usd.md) - Total contract value

---

## Derived Metrics

### Net New Rate (by Revenue)
```
Net New Booking Amount USD / (Renewal Booking Amount USD + Net New Booking Amount USD)
```

### Revenue Mix
```
Total Booking Amount USD = Renewal Booking Amount USD + Net New Booking Amount USD
```

### Net New Growth Rate
```
(Current Period Net New Amount - Prior Period Net New Amount) / Prior Period Net New Amount
```

---

## Data Quality Considerations

- Ensure is_renewal flag is properly populated (0 or 1)
- Verify net new classification is accurate
- Confirm booking_amount_usd is non-negative
- Validate that renewal + net new equals total booking amount

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
