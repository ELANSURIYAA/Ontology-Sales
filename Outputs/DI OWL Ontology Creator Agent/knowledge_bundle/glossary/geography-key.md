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

Geography Key is a system-generated unique identifier used to establish relationships between the geography dimension and booking transaction fact records. It serves as the primary key for geography records and enables efficient data integration and referential integrity.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_geography

**Source Column**: geography_key

**Entity**: [Geography](../entities/geography.md)

**Attribute**: Geography Key

**Data Type**: Integer

**Confidence Score**: 1.00

---

## Related Concepts

- [Geography](geography.md)
- [Booking Transaction](booking-transaction.md)

---

## Usage Context

Geography Key is used to:
- Uniquely identify geography records
- Link booking transactions to geographies
- Maintain referential integrity
- Enable efficient joins between fact and dimension tables
- Support data warehouse operations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Geography](../entities/geography.md)
- [Back to Main Index](../index.md)
