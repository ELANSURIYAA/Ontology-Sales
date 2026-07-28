---
title: Date
type: entity
description: Business entity representing calendar and fiscal reporting dates for booking analysis.
resource: entities
tags: [entity, date, fiscal, bookings]
timestamp: 2026-07-28
---

# Date

## Business Definition
Stores calendar and fiscal date attributes used to analyze bookings over time.

## Technical Mapping
- Source Table: `QuoteToBooking.dim_date`
- Related Glossary: [Date](../glossary/date.md)

## Attributes
- Date Key
- Full Date
- Month Name
- Calendar Year
- Fiscal Year
- Fiscal Quarter
- Fiscal Period Sequence

## Primary Keys
- Date Key

## Foreign Keys
None

## Measures
None

## Relationships
- [Date to Booking Transaction](../relationships/date-to-booking-transaction.md)

## Related Concepts
- [Full Date](../glossary/full-date.md)
- [Month Name](../glossary/month-name.md)
- [Calendar Year](../glossary/calendar-year.md)
- [Fiscal Year](../glossary/fiscal-year.md)
- [Fiscal Quarter](../glossary/fiscal-quarter.md)
- [Fiscal Period Sequence](../glossary/fiscal-period-sequence.md)
- [Booking Transaction](booking-transaction.md)
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

## Business Rules
- Each date record is uniquely identified by Date Key.
- Date records support both calendar and fiscal reporting analysis.
- A date may be associated with multiple booking transactions.
