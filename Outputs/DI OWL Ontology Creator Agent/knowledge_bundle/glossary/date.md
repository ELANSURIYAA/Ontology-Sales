---
title: Date
type: glossary
description: Calendar and fiscal date attributes used to analyze bookings over time
resource: glossary
tags: [glossary, date, time, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Date

## Business Definition

Stores calendar and fiscal date attributes used to analyze bookings over time.

## Business Meaning

The Date entity provides temporal context for booking transactions, enabling time-based analysis across calendar and fiscal periods. Date attributes support trending, period-over-period comparisons, and fiscal reporting.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_date  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Entity-level term  
**Confidence Score**: 1.00

## Synonyms

- Time
- Date Dimension
- Calendar

## Related Concepts

- [Date Key](./date-key.md)
- [Full Date](./full-date.md)
- [Fiscal Year](./fiscal-year.md)
- [Fiscal Quarter](./fiscal-quarter.md)
- [Booking Transaction](./booking-transaction.md)

## Usage Context

Date is used to:
- Enable time-based analysis of bookings
- Support fiscal and calendar reporting
- Track trends and patterns over time
- Enable period-over-period comparisons

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Date (ENT003)
