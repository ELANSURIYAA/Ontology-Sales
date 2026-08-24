---
title: Total TCV USD
type: measure
description: Total contract value in US dollars
resource: measures
tags: [tcv, revenue, metric, usd, contract]
timestamp: 2026-07-28T00:00:00Z
---

# Total TCV USD

## Business Definition

Total contract value in US dollars.

This measure represents the full contract value over the entire contract term, providing visibility into the total committed revenue from booking transactions.

---

## Formula

```sql
SUM(bookings.tcv_usd)
```

---

## Aggregation

**Type**: SUM

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

- [Total Contract Value](../glossary/total-contract-value.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Usage

This measure is used to:
- Track total committed contract revenue
- Analyze multi-year contract values
- Support long-term revenue forecasting
- Calculate contract lifetime value
- Monitor total pipeline and backlog value

---

## Technical Details

**Dialect**: ANSI_SQL

**Source Field**: bookings.tcv_usd

**Null Handling**: Sums only non-null tcv_usd values

**Currency**: US Dollars (USD)

**Calculation**: Total value over full contract term

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Catalog](../metrics.md)
