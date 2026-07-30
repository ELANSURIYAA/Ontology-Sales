---
title: Dates Domain
type: domain
description: Calendar and fiscal time attributes used to analyze bookings across reporting periods, years, quarters, and months
resource: domains
tags: [dates, time, calendar, fiscal, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Dates Domain

## Business Definition

The Dates domain provides calendar and fiscal time attributes used to analyze bookings across reporting periods, years, quarters, and months. This domain enables time-based analysis and trend reporting.

---

## Business Purpose

The Dates domain enables analysis of:

- Time-series trend analysis
- Year-over-year comparisons
- Quarter-over-quarter performance
- Fiscal period reporting
- Seasonal pattern identification
- Historical performance tracking

---

## Domain Type

**Dimension Domain** - Time attributes for temporal analysis

---

## Related Entities

- [Date](../entities/dates.md)

---

## Related Measures

All booking and revenue measures can be analyzed across time:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Total Quantity](../measures/total-quantity.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

---

## Related Relationships

- [Bookings to Dates](../relationships/bookings-to-dates.md)

---

## Key Concepts

### Calendar Year
Standard calendar year for annual reporting and comparison.

### Fiscal Year
Fiscal year used for financial and sales reporting aligned to business cycles.

### Fiscal Quarter
Fiscal quarter used for period-based reporting and quarterly business reviews.

### Fiscal Period Sequence
Sequential number representing the fiscal reporting period in chronological order.

---

## Semantic Links

### Related Domains
- [Bookings Domain](bookings.md) - Time-based booking analysis

### Related Glossary
- [Calendar Year](../glossary/calendar-year.md)
- [Fiscal Year](../glossary/fiscal-year.md)
- [Fiscal Quarter](../glossary/fiscal-quarter.md)
- [Fiscal Period Sequence](../glossary/fiscal-period-seq.md)

---

## Technical Mapping

**Source Table**: quotetobooking.dim_date  
**Primary Key**: date_key  
**Date Key Format**: YYYYMMDD

---

## Navigation

- [Return to Domains Index](index.md)
- [Return to Main Index](../index.md)
- [View Date Entity](../entities/dates.md)
