---
title: Dates
type: entity
description: Calendar and fiscal time attributes for reporting periods, years, quarters, and months
resource: entities
tags: [dates, dimension, time, calendar, fiscal]
timestamp: 2026-07-28T00:00:00Z
---

# Dates

## Business Definition

Provides calendar and fiscal time attributes used to analyze bookings across reporting periods, years, quarters, and months.

Dates enable time-based analysis and trending of booking transactions across calendar and fiscal reporting periods.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_date

**Source Columns**: date_key, full_date, month_name, calendar_year, fiscal_year, fiscal_quarter, fiscal_period_seq

---

## Attributes

- **date_key** - Intelligent date key in YYYYMMDD form used to join booking records to the date dimension
- **full_date** - Actual calendar date represented by the date record
- **month_name** - Name of the calendar month for the date
- **calendar_year** - Calendar year associated with the date
- **fiscal_year** - Fiscal year used for financial and sales reporting
- **fiscal_quarter** - Fiscal quarter used for period-based reporting and analysis
- **fiscal_period_seq** - Sequential number representing the fiscal reporting period in order

---

## Primary Keys

- date_key

---

## Foreign Keys

None

---

## Relationships

- [Bookings to Dates](../relationships/bookings-to-dates.md)

---

## Measures

All booking-related measures can be analyzed by time attributes:
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Booking Count](../measures/booking-count.md)

---

## Related Concepts

- [Fiscal Period](../glossary/fiscal-period.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

- Each date must have a unique date_key in YYYYMMDD format
- date_key serves as an intelligent key for efficient joins
- Dates support both calendar and fiscal reporting hierarchies
- fiscal_period_seq enables sequential period-based analysis
- Time-based analysis uses booking date as the primary time dimension
- Supports year-over-year, quarter-over-quarter, and month-over-month trending

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
