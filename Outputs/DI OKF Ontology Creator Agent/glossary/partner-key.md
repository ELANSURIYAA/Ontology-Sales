---
title: Partner Key
type: glossary
description: Surrogate key that uniquely identifies a partner record in the partner dimension
resource: glossary
tags: [okf, glossary, attribute, partner, key]
timestamp: 2026-07-28T00:00:00Z
---

# Partner Key

## Business Definition

Surrogate key that uniquely identifies a partner record in the partner dimension.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_partner  
**Source Column**: partner_key  
**Entity**: Partner Dimension  
**Attribute**: Partner Key

---

## Business Meaning

The Partner Key is a system-generated unique identifier used to link booking transactions to their associated partner attributes. It serves as the primary key in the Partner Dimension and as a foreign key in the Booking Fact table.

---

## Related Concepts

- [Partner Dimension](partner-dimension.md)
- [Booking Fact](booking-fact.md)

---

## Navigation

- [Back to Glossary Index](index.md)
- [Back to Bundle Index](../index.md)
