---
title: Geography Key
type: glossary
description: Surrogate key that uniquely identifies a geography record in the geography dimension
resource: glossary
tags: [geography, key, identifier, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Geography Key

## Business Definition

Surrogate key that uniquely identifies a geography record in the geography dimension.

---

## Business Meaning

Geography Key is a system-generated unique identifier used to link geography records to booking transactions. It serves as the primary key for the geography dimension and enables efficient spatial joins in analytical queries.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_geography  
**Source Column:** geography_key  
**Data Type:** Integer  
**Entity:** [Geography](../entities/geography.md)  
**Attribute:** Geography Key  
**Confidence Score:** 1.00

---

## Related Concepts

- [Geography](./geography.md) - Parent entity
- [Booking Transaction](./booking-transaction.md) - Uses geography key as foreign key

---

## Usage Context

Geography Key is used to:
- Uniquely identify each geography record
- Link booking transactions to geographic attributes
- Enable spatial analysis
- Support referential integrity in the data model

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/geography.md)
- [Return to Bundle Index](../index.md)
