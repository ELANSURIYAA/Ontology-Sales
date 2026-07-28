---
title: Booking Date Key
type: glossary
description: Foreign key linking the booking transaction to the reporting date dimension
resource: glossary
tags: [glossary, booking, date, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Date Key

## Business Definition

Foreign key linking the booking transaction to the reporting date dimension.

---

## Business Meaning

Booking Date Key is the foreign key that links each booking transaction to its corresponding date in the date dimension. This relationship enables time-based analysis of bookings, including fiscal and calendar period reporting, trend analysis, and period-over-period comparisons.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Source Column**: date_key

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Attribute**: Booking Date Key

**Data Type**: Integer

**Confidence Score**: 1.00

---

## Related Concepts

- [Booking Transaction](booking-transaction.md)
- [Date](date.md)
- [Date Key](date-key.md)

---

## Usage Context

Booking Date Key is used to:
- Link bookings to dates
- Enable time-based analysis
- Support fiscal and calendar reporting
- Facilitate trend analysis
- Enable period comparisons

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [View Entity: Date](../entities/date.md)
- [Back to Main Index](../index.md)
