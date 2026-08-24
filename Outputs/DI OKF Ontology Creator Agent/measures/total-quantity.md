---
title: Total Quantity
type: measure
description: Total number of units, licenses, or services booked
resource: measures
tags: [quantity, volume, metric]
timestamp: 2026-07-28T00:00:00Z
---

# Total Quantity

## Business Definition

Total number of units, licenses, or services booked.

This measure provides the aggregate quantity of items sold across booking transactions, enabling volume-based analysis independent of revenue values.

---

## Formula

```sql
SUM(bookings.quantity)
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
- Track unit sales volume
- Analyze product adoption and penetration
- Calculate average selling price per unit
- Monitor license or subscription quantities
- Compare volume performance across products and segments

---

## Technical Details

**Dialect**: ANSI_SQL

**Source Field**: bookings.quantity

**Null Handling**: Sums only non-null quantity values

**Unit of Measure**: Units, licenses, or services

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Catalog](../metrics.md)
