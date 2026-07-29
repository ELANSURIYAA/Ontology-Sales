---
title: Partner Key
type: glossary
description: Surrogate key that uniquely identifies a partner record in the partner dimension
resource: glossary
tags: [glossary, partner, key, identifier]
timestamp: 2026-07-28T00:00:00Z
---

# Partner Key

## Business Definition

Surrogate key that uniquely identifies a partner record in the partner dimension.

## Business Meaning

The Partner Key is a system-generated unique identifier used to link partner dimension records to booking transaction fact records. It serves as the primary key for the partner dimension and enables efficient joins and referential integrity in the dimensional model.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_partner  
**Source Column**: partner_key  
**Entity**: [Partner](../entities/partner.md)  
**Attribute**: Partner Key  
**Data Type**: Integer  
**Confidence Score**: 1.00

## Synonyms

- Partner Identifier
- Partner Surrogate Key

## Related Concepts

- [Partner](./partner.md)
- [Booking Transaction](./booking-transaction.md)

## Usage Context

The Partner Key is used to:
- Uniquely identify partner records
- Link partners to booking transactions
- Maintain referential integrity
- Enable efficient dimensional queries

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Partner (ENT005)  
**Attribute**: ATTR025
