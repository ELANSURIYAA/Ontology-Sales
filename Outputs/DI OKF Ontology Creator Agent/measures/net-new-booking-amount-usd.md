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

Total booked sales amount in US dollars for non-renewal transactions.

This measure isolates revenue from new business bookings, enabling analysis of new customer acquisition and expansion revenue performance.

---

## Formula

```sql
SUM(CASE WHEN bookings.is_renewal = 0 THEN bookings.booking_amount_usd ELSE 0 END)
```

---

## Aggregation

**Type**: CONDITIONAL SUM

**Grain**: Booking transaction

---

## Related Entities

- [Bookings](../entities/bookings.md)

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Related Concepts

- [Net New Business](../glossary/net-new-business.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Usage

This measure is used to:
- Track new business revenue performance
- Analyze customer acquisition effectiveness
- Monitor expansion and upsell revenue
- Calculate new business growth rates
- Support sales pipeline and forecasting

---

## Technical Details

**Dialect**: ANSI_SQL

**Source Fields**: bookings.is_renewal, bookings.booking_amount_usd

**Null Handling**: Treats null or zero is_renewal as non-renewal

**Currency**: US Dollars (USD)

**Filter Condition**: is_renewal = 0

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Catalog](../metrics.md)
