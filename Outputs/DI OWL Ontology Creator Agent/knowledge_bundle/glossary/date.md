---
title: Date
type: glossary
description: Stores calendar and fiscal date attributes used to analyze bookings over time
resource: glossary
tags: [date, time, calendar, fiscal, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Date

## Business Definition

Stores calendar and fiscal date attributes used to analyze bookings over time.

---

## Business Meaning

The Date entity provides temporal context for booking transactions, enabling time-based analysis across calendar and fiscal periods. It supports trend analysis, period comparisons, and time-series reporting.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_date  
**Entity:** [Date](../entities/date.md)  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Transactions occurring on dates
- [Date Key](./date-key.md) - Unique identifier
- [Fiscal Year](./fiscal-year.md) - Fiscal year attribute
- [Fiscal Quarter](./fiscal-quarter.md) - Fiscal quarter attribute
- [Calendar Year](./calendar-year.md) - Calendar year attribute

---

## Usage Context

Date is used to:
- Provide temporal context for transactions
- Enable time-based analysis and reporting
- Support fiscal and calendar period analysis
- Track trends and patterns over time

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/date.md)
- [Return to Bundle Index](../index.md)
