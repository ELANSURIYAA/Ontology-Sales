---
title: Booking Count
type: measure
description: Count of booking transaction records
resource: measures
tags: [booking-count, volume, metric]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Count

## Business Definition

Count of booking transaction records.

This measure provides the total number of individual booking transactions, enabling volume-based analysis of sales activity.

---

## Formula

```sql
COUNT(bookings.booking_id)
```

---

## Aggregation

**Type**: COUNT

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
- Track sales activity volume
- Analyze booking transaction frequency
- Monitor sales velocity and throughput
- Compare transaction volumes across dimensions
- Calculate average values per transaction

---

## Technical Details

**Dialect**: ANSI_SQL

**Source Field**: bookings.booking_id

**Null Handling**: Counts only non-null booking_id values

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Catalog](../metrics.md)
