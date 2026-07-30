---
title: Date
type: entity
description: Calendar and fiscal time attributes used to analyze bookings across reporting periods, years, quarters, and months
resource: entities
tags: [date, time, calendar, fiscal, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Date

## Business Definition

The Date entity provides calendar and fiscal time attributes used to analyze bookings across reporting periods, years, quarters, and months. This entity enables time-based analysis and trend reporting.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_date  
**Source Schema**: quotetobooking  
**Entity Type**: Dimension  
**Grain**: One row per date

---

## Attributes

- date_key
- full_date
- month_name
- calendar_year
- fiscal_year
- fiscal_quarter
- fiscal_period_seq

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

All booking and revenue measures can be analyzed across time:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Total Quantity](../measures/total-quantity.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

---

## Related Concepts

- [Calendar Year](../glossary/calendar-year.md)
- [Fiscal Year](../glossary/fiscal-year.md)
- [Fiscal Quarter](../glossary/fiscal-quarter.md)
- [Fiscal Period Sequence](../glossary/fiscal-period-seq.md)

---

## Business Rules

### Date Key Format
Date key is stored in YYYYMMDD intelligent key format for efficient joining and filtering.

### Calendar vs Fiscal
Calendar attributes represent standard calendar periods while fiscal attributes align to business reporting cycles.

### Fiscal Period Sequence
Fiscal period sequence provides a sequential number for chronological ordering of fiscal periods.

### Time Hierarchy
Date supports multiple time hierarchies: Calendar (Year → Month) and Fiscal (Year → Quarter → Period).

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Dates Domain](../domains/dates.md)
