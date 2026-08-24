---
title: Renewal Booking Amount USD
type: measure
description: Total booked sales amount in US dollars for renewal transactions
resource: measures
tags: [renewal, revenue, metric, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Renewal Booking Amount USD

## Business Definition

Renewal Booking Amount USD represents the total booked sales amount in US dollars for renewal transactions. This measure isolates revenue from existing customer renewals, providing insight into customer retention and recurring revenue performance.

---

## Formula

**Expression**: SUM(CASE WHEN bookings.is_renewal = 1 THEN bookings.booking_amount_usd ELSE 0 END)

**Dialect**: ANSI_SQL

**Aggregation Type**: Conditional SUM

---

## Business Purpose

This measure enables:

- **Retention Analysis**: Track revenue from customer renewals
- **Recurring Revenue**: Monitor recurring revenue from existing customers
- **Churn Analysis**: Evaluate customer retention and renewal rates
- **Revenue Mix**: Understand the balance between renewal and new business
- **Customer Success**: Measure effectiveness of customer retention strategies
- **Forecasting**: Project future renewal revenue based on historical patterns

---

## Related Entities

**Primary Entity**: [Bookings](../entities/bookings.md)

**Dimensional Analysis**: This measure can be analyzed across all dimension entities:
- [Customers](../entities/customers.md) - Renewal revenue by customer segment, industry, account tier
- [Products](../entities/products.md) - Renewal revenue by product family, technology domain, offer type
- [Partners](../entities/partners.md) - Renewal revenue by partner type, tier, route to market
- [Geographies](../entities/geographies.md) - Renewal revenue by region, theater, country
- [Sales Representatives](../entities/sales-representatives.md) - Renewal revenue by sales role, team
- [Contracts](../entities/contracts.md) - Renewal revenue by contract type, term, coverage level
- [Dates](../entities/dates.md) - Renewal revenue by fiscal year, quarter, month

---

## Related Concepts

- [Renewal](../glossary/renewal.md)
- [Booking Amount](../glossary/booking-amount.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Calculation Logic

The measure sums the booking_amount_usd field only for records where is_renewal equals 1:

```
Renewal Booking Amount = SUM(booking_amount_usd WHERE is_renewal = 1)
```

The is_renewal flag indicates whether a booking transaction represents a renewal (1) or net new business (0).

---

## Usage Examples

### Renewal Revenue by Fiscal Year
```sql
SELECT 
    dates.fiscal_year,
    SUM(CASE WHEN bookings.is_renewal = 1 THEN bookings.booking_amount_usd ELSE 0 END) as renewal_amount
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.fiscal_year
```

### Renewal Revenue by Customer Segment
```sql
SELECT 
    customers.segment,
    SUM(CASE WHEN bookings.is_renewal = 1 THEN bookings.booking_amount_usd ELSE 0 END) as renewal_amount
FROM bookings
JOIN customers ON bookings.customer_key = customers.customer_key
GROUP BY customers.segment
```

---

## Business Rules

1. **Renewal Flag**: Only bookings with is_renewal = 1 are included
2. **Non-Negative Values**: Renewal amounts must be non-negative
3. **Currency**: All amounts are in US dollars
4. **Additive Measure**: Amounts can be summed across all dimensions
5. **Mutually Exclusive**: A booking is either renewal or net new, not both

---

## Related Measures

- [Net New Booking Amount USD](./net-new-booking-amount-usd.md) - Complementary measure for new business
- [Total Booking Amount USD](./total-booking-amount-usd.md) - Total revenue (renewal + net new)
- [Total ACV USD](./total-acv-usd.md) - Annual contract value
- [Total TCV USD](./total-tcv-usd.md) - Total contract value

---

## Derived Metrics

### Renewal Rate (by Revenue)
```
Renewal Booking Amount USD / (Renewal Booking Amount USD + Net New Booking Amount USD)
```

### Revenue Mix
```
Total Booking Amount USD = Renewal Booking Amount USD + Net New Booking Amount USD
```

### Renewal Growth Rate
```
(Current Period Renewal Amount - Prior Period Renewal Amount) / Prior Period Renewal Amount
```

---

## Data Quality Considerations

- Ensure is_renewal flag is properly populated (0 or 1)
- Verify renewal classification is accurate
- Confirm booking_amount_usd is non-negative
- Validate that renewal + net new equals total booking amount

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
