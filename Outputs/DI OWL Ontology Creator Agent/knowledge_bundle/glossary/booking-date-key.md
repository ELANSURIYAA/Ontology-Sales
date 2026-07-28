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

Booking Date Key connects each booking transaction to a specific date in the date dimension. This link enables time-based analysis of bookings across calendar and fiscal periods, supporting trending, period comparisons, and temporal reporting.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: fact_bookings  
**Source Column**: date_key  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Booking Date Key  
**Data Type**: integer  
**Nullable**: Yes  
**Foreign Key**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Transaction Date Key
- Date Foreign Key

---

## Related Concepts

### Related Entities
- [Booking Transaction](../entities/booking-transaction.md)
- [Date](../entities/date.md)

### Related Relationships
- [Date to Booking Transaction](../relationships/date-to-booking-transaction.md)

---

## Usage Context

Booking Date Key is used to:
- Link transactions to dates
- Enable time-based analysis
- Support fiscal reporting

---

## Navigation

- [View Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [View Date Entity](../entities/date.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Booking Transaction  
**Source Attribute**: Booking Date Key  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
