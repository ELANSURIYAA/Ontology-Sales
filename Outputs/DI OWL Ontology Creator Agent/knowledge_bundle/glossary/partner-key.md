---
title: Partner Key
type: glossary
description: Surrogate key that uniquely identifies a partner record in the partner dimension
resource: glossary
tags: [partner, key, identifier, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Partner Key

## Business Definition

Surrogate key that uniquely identifies a partner record in the partner dimension.

---

## Business Meaning

Partner Key is a system-generated unique identifier used to link partner records to booking transactions. It serves as the primary key for the partner dimension and enables efficient joins in analytical queries.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_partner  
**Source Column:** partner_key  
**Data Type:** Integer  
**Entity:** [Partner](../entities/partner.md)  
**Attribute:** Partner Key  
**Confidence Score:** 1.00

---

## Related Concepts

- [Partner](./partner.md) - Parent entity
- [Booking Transaction](./booking-transaction.md) - Uses partner key as foreign key
- [Partner ID](./partner-id.md) - Business identifier

---

## Usage Context

Partner Key is used to:
- Uniquely identify each partner record
- Link booking transactions to partner attributes
- Enable dimensional analysis by partner characteristics
- Support referential integrity in the data model

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/partner.md)
- [Return to Bundle Index](../index.md)
