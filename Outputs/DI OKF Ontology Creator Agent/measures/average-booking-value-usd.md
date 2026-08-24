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

Average booking value in US dollars per distinct booking transaction.

This measure calculates the average revenue value per booking transaction, providing insight into deal size and transaction value patterns.

---

## Formula

```sql
SUM(bookings.booking_amount_usd) / NULLIF(COUNT(DISTINCT bookings.booking_id), 0)
```

---

## Aggregation

**Type**: CALCULATED (SUM / COUNT DISTINCT)

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
- Analyze average deal size
- Track transaction value trends
- Compare deal sizes across segments and channels
- Support pricing and packaging strategies
- Monitor sales effectiveness and deal quality

---

## Technical Details

**Dialect**: ANSI_SQL

**Source Fields**: bookings.booking_amount_usd, bookings.booking_id

**Null Handling**: Uses NULLIF to prevent division by zero

**Currency**: US Dollars (USD)

**Calculation**: Total revenue divided by distinct booking count

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Catalog](../metrics.md)
