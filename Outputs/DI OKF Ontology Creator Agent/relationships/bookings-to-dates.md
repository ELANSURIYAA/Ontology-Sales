---
title: Bookings to Dates
type: relationship
description: Links booking transactions to calendar and fiscal time periods
resource: relationships
tags: [bookings, dates, relationship, many-to-one]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Dates

## Business Definition

Links booking transactions to calendar and fiscal time attributes used to analyze bookings across reporting periods, years, quarters, and months.

This relationship enables time-based analysis and trending of booking performance across calendar and fiscal reporting periods.

---

## Relationship Type

**many-to-one**

Multiple booking transactions can occur on the same date.

---

## Source Entity

[Bookings](../entities/bookings.md)

---

## Target Entity

[Dates](../entities/dates.md)

---

## Cardinality

- Each booking transaction must be associated with exactly one date record
- Each date record can be associated with multiple booking transactions

---

## Technical Mapping

**Join Condition**: bookings.date_key = dates.date_key

**Left Dataset**: bookings (quotetobooking.fact_bookings)

**Right Dataset**: dates (quotetobooking.dim_date)

**Join Keys**:
- Left: date_key
- Right: date_key

---

## Business Purpose

This relationship enables:
- Time-series analysis of booking trends
- Fiscal year and quarter-based reporting
- Month-over-month and year-over-year comparisons
- Seasonal pattern analysis
- Period-based forecasting and planning
- Calendar vs fiscal period reconciliation

---

## Related Measures

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Booking Count](../measures/booking-count.md)

---

## Related Concepts

- [Fiscal Period](../glossary/fiscal-period.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
