---
title: Partner Key
type: glossary
description: Surrogate key that uniquely identifies a partner record in the partner dimension
resource: glossary
tags: [glossary, partner, key, identifier, surrogate-key]
timestamp: 2026-07-28T00:00:00Z
---

# Partner Key

## Business Definition

Surrogate key that uniquely identifies a partner record in the partner dimension.

---

## Business Meaning

Partner Key is a system-generated unique identifier used to link partner records to booking transactions. It serves as the primary key for the partner dimension and enables efficient joins and referential integrity in the data model.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_partner  
**Source Column**: partner_key  
**Entity**: [Partner](../entities/partner.md)  
**Attribute**: Partner Key  
**Data Type**: integer  
**Nullable**: No  
**Primary Key**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Partner Identifier
- Partner Surrogate Key

---

## Related Concepts

### Related Entities
- [Partner](../entities/partner.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Relationships
- [Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)

---

## Usage Context

Partner Key is used to:
- Uniquely identify partner records
- Link booking transactions to partners
- Enable dimensional analysis by partner attributes
- Maintain referential integrity

---

## Navigation

- [View Glossary Index](index.md)
- [View Partner Entity](../entities/partner.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Partner  
**Source Attribute**: Partner Key  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
