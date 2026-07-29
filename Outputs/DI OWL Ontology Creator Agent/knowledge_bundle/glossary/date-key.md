---
title: Date Key
type: glossary
description: Encoded key that uniquely identifies a reporting date in the date dimension
resource: glossary
tags: [date, key, identifier, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Date Key

## Business Definition

Encoded key that uniquely identifies a reporting date in the date dimension.

---

## Business Meaning

Date Key is a system-generated unique identifier used to link date records to booking transactions. It serves as the primary key for the date dimension and enables efficient temporal joins in analytical queries.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_date  
**Source Column:** date_key  
**Data Type:** Integer  
**Entity:** [Date](../entities/date.md)  
**Attribute:** Date Key  
**Confidence Score:** 0.95

---

## Related Concepts

- [Date](./date.md) - Parent entity
- [Booking Transaction](./booking-transaction.md) - Uses date key as foreign key
- [Booking Date Key](./booking-date-key.md) - Foreign key reference

---

## Usage Context

Date Key is used to:
- Uniquely identify each date record
- Link booking transactions to date attributes
- Enable temporal analysis
- Support referential integrity in the data model

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/date.md)
- [Return to Bundle Index](../index.md)
