---
title: Average Discount Pct
type: measure
description: Average discount applied to booked items or services, stored as a fractional percentage
resource: measures
tags: [discount, pricing, metric, percentage]
timestamp: 2026-07-28T00:00:00Z
---

# Average Discount Pct

## Business Definition

Average discount applied to booked items or services, stored as a fractional percentage.

This measure provides insight into pricing strategies and discount practices across booking transactions.

---

## Formula

```sql
AVG(bookings.discount_pct)
```

---

## Aggregation

**Type**: AVERAGE

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
- Monitor discount levels and pricing discipline
- Analyze discount patterns across segments and products
- Support pricing optimization strategies
- Track promotional effectiveness
- Compare discount practices across sales channels

---

## Technical Details

**Dialect**: ANSI_SQL

**Source Field**: bookings.discount_pct

**Null Handling**: Averages only non-null discount_pct values

**Format**: Fractional percentage (e.g., 0.15 represents 15% discount)

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Catalog](../metrics.md)
