---
title: Date
type: glossary
description: Calendar and fiscal date attributes used to analyze bookings over time
resource: glossary
tags: [glossary, date, time, calendar, fiscal]
timestamp: 2026-07-28T00:00:00Z
---

# Date

## Business Definition

Stores calendar and fiscal date attributes used to analyze bookings over time.

---

## Business Meaning

The Date entity provides temporal context for booking transactions, enabling time-based analysis across both calendar and fiscal periods. It supports trending, period-over-period comparisons, seasonal analysis, and fiscal reporting requirements.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_date  
**Entity**: [Date](../entities/date.md)  
**Confidence Score**: 1.00

---

## Synonyms

- Time
- Date Dimension
- Calendar
- Time Period

---

## Related Concepts

### Related Entities
- [Date](../entities/date.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Date Key](date-key.md)
- [Full Date](full-date.md)
- [Month Name](month-name.md)
- [Calendar Year](calendar-year.md)
- [Fiscal Year](fiscal-year.md)
- [Fiscal Quarter](fiscal-quarter.md)
- [Fiscal Period Sequence](fiscal-period-sequence.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)

---

## Usage Context

Date is used to:
- Enable time-based analysis of bookings
- Support fiscal and calendar reporting
- Track trends and growth over time
- Enable period-over-period comparisons

---

## Navigation

- [View Glossary Index](index.md)
- [View Date Entity](../entities/date.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Entity  
**Source Entity**: Date  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
