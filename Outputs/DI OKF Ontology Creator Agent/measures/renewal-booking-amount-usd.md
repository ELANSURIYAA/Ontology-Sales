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

Total booked sales amount in US dollars for renewal transactions.

This measure isolates revenue from renewal bookings, enabling analysis of customer retention and recurring revenue performance.

---

## Formula

```sql
SUM(CASE WHEN bookings.is_renewal = 1 THEN bookings.booking_amount_usd ELSE 0 END)
```

---

## Aggregation

**Type**: CONDITIONAL SUM

**Grain**: Booking transaction

---

## Related Entities

- [Bookings](../entities/bookings.md)
- [Contracts](../entities/contracts.md)

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Related Concepts

- [Renewal](../glossary/renewal.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Usage

This measure is used to:
- Track renewal revenue performance
- Analyze customer retention and loyalty
- Monitor recurring revenue streams
- Calculate renewal rates and retention metrics
- Support customer success and renewal forecasting

---

## Technical Details

**Dialect**: ANSI_SQL

**Source Fields**: bookings.is_renewal, bookings.booking_amount_usd

**Null Handling**: Treats null or zero is_renewal as non-renewal

**Currency**: US Dollars (USD)

**Filter Condition**: is_renewal = 1

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Catalog](../metrics.md)
