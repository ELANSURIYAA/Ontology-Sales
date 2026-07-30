---
title: Bookings to Dates
type: relationship
description: Links booking transactions to the date when the booking occurred
resource: relationships
tags: [bookings, dates, relationship, many-to-one]
timestamp: 2024-01-15T00:00:00Z
---

# Bookings to Dates

## Business Definition

This relationship links booking transactions to the date when the booking occurred, enabling time-based analysis of bookings across calendar and fiscal periods, years, quarters, and months.

---

## Relationship Details

**Source Entity**: [Booking Transaction](../entities/bookings.md)  
**Target Entity**: [Date](../entities/dates.md)  
**Relationship Type**: Many-to-One  
**Cardinality**: Many bookings can occur on one date

---

## Technical Mapping

**Join Type**: Inner Join  
**Left Key**: bookings.date_key  
**Right Key**: dates.date_key

---

## Business Description

Each booking transaction is associated with a specific date that represents when the booking occurred. Date attributes include calendar year, fiscal year, fiscal quarter, fiscal period sequence, and month name. Multiple booking transactions can occur on the same date. This relationship is essential for time-series analysis and trend reporting.

---

## Usage

This relationship enables analysis such as:

- Year-over-year booking trends
- Quarter-over-quarter performance
- Fiscal period reporting
- Monthly booking patterns
- Seasonal trend analysis
- Historical performance tracking

---

## Related Concepts

- [Calendar Year](../glossary/calendar-year.md)
- [Fiscal Year](../glossary/fiscal-year.md)
- [Fiscal Quarter](../glossary/fiscal-quarter.md)
- [Fiscal Period Sequence](../glossary/fiscal-period-seq.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Date Entity](../entities/dates.md)
- [View Dates Domain](../domains/dates.md)
