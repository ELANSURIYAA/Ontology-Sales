---
title: Average Selling Price USD
type: measure
description: Average booked revenue per unit sold in US dollars
resource: measures
tags: [selling-price, pricing, metric, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Average Selling Price USD

## Business Definition

Average booked revenue per unit sold in US dollars.

This measure calculates the average price realized per unit, license, or service sold, reflecting the net pricing after discounts.

---

## Formula

```sql
SUM(bookings.booking_amount_usd) / NULLIF(SUM(bookings.quantity), 0)
```

---

## Aggregation

**Type**: CALCULATED (SUM / SUM)

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
- Analyze realized pricing per unit
- Track pricing trends over time
- Compare pricing across products and segments
- Monitor price realization and discount impact
- Support pricing strategy and optimization

---

## Technical Details

**Dialect**: ANSI_SQL

**Source Fields**: bookings.booking_amount_usd, bookings.quantity

**Null Handling**: Uses NULLIF to prevent division by zero

**Currency**: US Dollars (USD)

**Calculation**: Total revenue divided by total quantity

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Catalog](../metrics.md)
