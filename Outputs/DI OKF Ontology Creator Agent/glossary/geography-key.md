---
title: Geography Key
type: glossary
description: Surrogate key that uniquely identifies a geography record in the geography dimension
resource: glossary
tags: [okf, glossary, attribute, geography, key]
timestamp: 2026-07-28T00:00:00Z
---

# Geography Key

## Business Definition

Surrogate key that uniquely identifies a geography record in the geography dimension.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_geography  
**Source Column**: geography_key  
**Entity**: Geography Dimension  
**Attribute**: Geography Key

---

## Business Meaning

The Geography Key is a system-generated unique identifier used to link booking transactions to their associated geographic attributes. It serves as the primary key in the Geography Dimension and as a foreign key in the Booking Fact table.

---

## Related Concepts

- [Geography Dimension](geography-dimension.md)
- [Booking Fact](booking-fact.md)

---

## Navigation

- [Back to Glossary Index](index.md)
- [Back to Bundle Index](../index.md)
