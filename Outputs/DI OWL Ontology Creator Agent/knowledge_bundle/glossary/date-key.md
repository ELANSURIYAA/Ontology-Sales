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

## Business Meaning

The Date Key is a system-generated unique identifier used to link date dimension records to booking transaction fact records. It serves as the primary key for the date dimension and enables efficient temporal joins in the dimensional model.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_date  
**Source Column**: date_key  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Date Key  
**Data Type**: Integer  
**Confidence Score**: 0.95

## Synonyms

- Date Identifier
- Date Surrogate Key
- Time Key

## Related Concepts

- [Date](./date.md)
- [Booking Transaction](./booking-transaction.md)
- [Booking Date Key](./booking-date-key.md)

## Usage Context

The Date Key is used to:
- Uniquely identify date records
- Link dates to booking transactions
- Maintain referential integrity
- Enable efficient temporal queries

---

**Confidence Score**: 0.95  
**Source**: OSI Semantic Model  
**Entity**: Date (ENT003)  
**Attribute**: ATTR014
