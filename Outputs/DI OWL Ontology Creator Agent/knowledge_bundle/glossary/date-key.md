---
title: Date Key
type: glossary
description: Encoded key that uniquely identifies a reporting date in the date dimension
resource: glossary
tags: [glossary, date, key, identifier]
timestamp: 2026-07-28T00:00:00Z
---

# Date Key

## Business Definition

Encoded key that uniquely identifies a reporting date in the date dimension.

---

## Business Meaning

Date Key is a system-generated unique identifier used to link date records to booking transactions. It serves as the primary key for the date dimension and enables efficient joins and referential integrity in the data model.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_date  
**Source Column**: date_key  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Date Key  
**Data Type**: integer  
**Nullable**: No  
**Primary Key**: Yes  
**Confidence Score**: 0.95

---

## Synonyms

- Date Identifier
- Date Surrogate Key
- Time Key

---

## Related Concepts

### Related Entities
- [Date](../entities/date.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Relationships
- [Date to Booking Transaction](../relationships/date-to-booking-transaction.md)

---

## Usage Context

Date Key is used to:
- Uniquely identify date records
- Link booking transactions to dates
- Enable time-based dimensional analysis
- Maintain referential integrity

---

## Navigation

- [View Glossary Index](index.md)
- [View Date Entity](../entities/date.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Date  
**Source Attribute**: Date Key  
**Confidence Score**: 0.95  
**Last Updated**: 2026-07-28T00:00:00Z
