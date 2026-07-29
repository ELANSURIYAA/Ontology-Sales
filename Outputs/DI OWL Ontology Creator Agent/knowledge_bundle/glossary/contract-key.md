---
title: Contract Key
type: glossary
description: Surrogate key that uniquely identifies a contract record in the contract dimension
resource: glossary
tags: [glossary, contract, key, identifier]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Key

## Business Definition

Surrogate key that uniquely identifies a contract record in the contract dimension.

## Business Meaning

The Contract Key is a system-generated unique identifier used to link contract dimension records to booking transaction fact records. It serves as the primary key for the contract dimension and enables efficient joins and referential integrity in the dimensional model.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract  
**Source Column**: contract_key  
**Entity**: [Contract](../entities/contract.md)  
**Attribute**: Contract Key  
**Data Type**: Integer  
**Confidence Score**: 1.00

## Synonyms

- Contract Identifier
- Contract Surrogate Key
- Contract ID

## Related Concepts

- [Contract](./contract.md)
- [Booking Transaction](./booking-transaction.md)

## Usage Context

The Contract Key is used to:
- Uniquely identify contract records
- Link contracts to booking transactions
- Maintain referential integrity
- Enable efficient dimensional queries

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Contract (ENT001)  
**Attribute**: ATTR001
