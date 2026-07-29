---
title: Geography Key
type: glossary
description: Surrogate key that uniquely identifies a geography record in the geography dimension
resource: glossary
tags: [glossary, geography, key, identifier]
timestamp: 2026-07-28T00:00:00Z
---

# Geography Key

## Business Definition

Surrogate key that uniquely identifies a geography record in the geography dimension.

## Business Meaning

The Geography Key is a system-generated unique identifier used to link geography dimension records to booking transaction fact records. It serves as the primary key for the geography dimension and enables efficient joins and referential integrity in the dimensional model.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_geography  
**Source Column**: geography_key  
**Entity**: [Geography](../entities/geography.md)  
**Attribute**: Geography Key  
**Data Type**: Integer  
**Confidence Score**: 1.00

## Synonyms

- Geography Identifier
- Geography Surrogate Key
- Location Key

## Related Concepts

- [Geography](./geography.md)
- [Booking Transaction](./booking-transaction.md)

## Usage Context

The Geography Key is used to:
- Uniquely identify geography records
- Link geographies to booking transactions
- Maintain referential integrity
- Enable efficient dimensional queries

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Geography (ENT004)  
**Attribute**: ATTR021
