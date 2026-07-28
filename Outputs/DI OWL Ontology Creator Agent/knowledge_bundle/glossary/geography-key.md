---
title: Geography Key
type: glossary
description: Surrogate key that uniquely identifies a geography record in the geography dimension
resource: glossary
tags: [glossary, geography, key, identifier, surrogate-key]
timestamp: 2026-07-28T00:00:00Z
---

# Geography Key

## Business Definition

Surrogate key that uniquely identifies a geography record in the geography dimension.

---

## Business Meaning

Geography Key is a system-generated unique identifier used to link geography records to booking transactions. It serves as the primary key for the geography dimension and enables efficient joins and referential integrity in the data model.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_geography  
**Source Column**: geography_key  
**Entity**: [Geography](../entities/geography.md)  
**Attribute**: Geography Key  
**Data Type**: integer  
**Nullable**: No  
**Primary Key**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Geography Identifier
- Geography Surrogate Key
- Location Key

---

## Related Concepts

### Related Entities
- [Geography](../entities/geography.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Relationships
- [Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)

---

## Usage Context

Geography Key is used to:
- Uniquely identify geography records
- Link booking transactions to geographies
- Enable dimensional analysis by geographic attributes
- Maintain referential integrity

---

## Navigation

- [View Glossary Index](index.md)
- [View Geography Entity](../entities/geography.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Geography  
**Source Attribute**: Geography Key  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
