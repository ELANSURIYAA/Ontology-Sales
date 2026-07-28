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

Partner Key is a system-generated unique identifier used to establish relationships between the partner dimension and booking transaction fact records. It serves as the primary key for partner records and enables efficient data integration and referential integrity.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_partner

**Source Column**: partner_key

**Entity**: [Partner](../entities/partner.md)

**Attribute**: Partner Key

**Data Type**: Integer

**Confidence Score**: 1.00

---

## Related Concepts

- [Partner](partner.md)
- [Booking Transaction](booking-transaction.md)

---

## Usage Context

Partner Key is used to:
- Uniquely identify partner records
- Link booking transactions to partners
- Maintain referential integrity
- Enable efficient joins between fact and dimension tables
- Support data warehouse operations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Partner](../entities/partner.md)
- [Back to Main Index](../index.md)
