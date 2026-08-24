---
title: Total ACV USD
type: measure
description: Total annual contract value in US dollars
resource: measures
tags: [acv, revenue, metric, usd, contract]
timestamp: 2026-07-28T00:00:00Z
---

# Total ACV USD

## Business Definition

Total annual contract value in US dollars.

This measure represents the annualized revenue value of booking transactions, normalizing contract values to an annual basis for consistent comparison and forecasting.

---

## Formula

```sql
SUM(bookings.acv_usd)
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

- [Annual Contract Value](../glossary/annual-contract-value.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Usage

This measure is used to:
- Track annualized revenue performance
- Normalize multi-year contracts to annual values
- Support recurring revenue analysis
- Enable consistent period-over-period comparisons
- Forecast annual revenue run rates

---

## Technical Details

**Dialect**: ANSI_SQL

**Source Field**: bookings.acv_usd

**Null Handling**: Sums only non-null acv_usd values

**Currency**: US Dollars (USD)

**Calculation**: Annualized value based on contract terms

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Catalog](../metrics.md)
