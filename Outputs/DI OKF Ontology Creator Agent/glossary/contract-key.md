---
title: Contract Key
type: glossary
description: Surrogate key that uniquely identifies a contract record in the contract dimension
resource: glossary
tags: [okf, glossary, attribute, contract, key]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Key

## Business Definition

Surrogate key that uniquely identifies a contract record in the contract dimension.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_contract  
**Source Column**: contract_key  
**Entity**: Contract Dimension  
**Attribute**: Contract Key

---

## Business Meaning

The Contract Key is a system-generated unique identifier used to link booking transactions to their associated contract attributes. It serves as the primary key in the Contract Dimension and as a foreign key in the Booking Fact table.

---

## Related Concepts

- [Contract Dimension](contract-dimension.md)
- [Booking Fact](booking-fact.md)

---

## Navigation

- [Back to Glossary Index](index.md)
- [Back to Bundle Index](../index.md)
