---
title: Distinct Order Count
type: measure
description: Count of distinct sales orders associated with booking transactions
resource: measures
tags: [order-count, volume, metric]
timestamp: 2026-07-28T00:00:00Z
---

# Distinct Order Count

## Business Definition

Count of distinct sales orders associated with booking transactions.

This measure provides the total number of unique sales orders, enabling analysis of order-level activity independent of the number of line items per order.

---

## Formula

```sql
COUNT(DISTINCT bookings.order_number)
```

---

## Aggregation

**Type**: COUNT DISTINCT

**Grain**: Sales order

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
- Track unique sales order volume
- Analyze order complexity (lines per order)
- Monitor order processing efficiency
- Compare order volumes across dimensions
- Calculate average values per order

---

## Technical Details

**Dialect**: ANSI_SQL

**Source Field**: bookings.order_number

**Null Handling**: Counts only distinct non-null order_number values

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Catalog](../metrics.md)
