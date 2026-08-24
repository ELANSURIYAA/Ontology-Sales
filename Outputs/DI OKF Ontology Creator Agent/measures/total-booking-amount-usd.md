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

Total booked sales amount in US dollars after pricing and discount adjustments.

This measure represents the net revenue value of booking transactions and is the primary revenue metric for sales performance analysis.

---

## Formula

```sql
SUM(bookings.booking_amount_usd)
```

---

## Aggregation

**Type**: SUM

**Grain**: Booking transaction

---

## Related Entities

- [Bookings](../entities/bookings.md)

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Related Concepts

- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Usage

This measure is used to:
- Track total sales revenue
- Analyze revenue performance across dimensions
- Calculate revenue growth and trends
- Monitor sales targets and quotas
- Support financial forecasting and planning

---

## Technical Details

**Dialect**: ANSI_SQL

**Source Field**: bookings.booking_amount_usd

**Null Handling**: Sums only non-null booking_amount_usd values

**Currency**: US Dollars (USD)

**Calculation**: Reflects net revenue after discounts

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Catalog](../metrics.md)
