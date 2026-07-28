---
title: Contract Key
type: glossary
description: Surrogate key that uniquely identifies a contract record in the contract dimension
resource: glossary
tags: [glossary, contract, key, identifier, surrogate-key]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Key

## Business Definition

Surrogate key that uniquely identifies a contract record in the contract dimension.

---

## Business Meaning

Contract Key is a system-generated unique identifier used to link contract records to booking transactions. It serves as the primary key for the contract dimension and enables efficient joins and referential integrity in the data model.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_contract  
**Source Column**: contract_key  
**Entity**: [Contract](../entities/contract.md)  
**Attribute**: Contract Key  
**Data Type**: integer  
**Nullable**: No  
**Primary Key**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Contract Identifier
- Contract ID
- Contract Surrogate Key

---

## Related Concepts

### Related Entities
- [Contract](../entities/contract.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Relationships
- [Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)

---

## Usage Context

Contract Key is used to:
- Uniquely identify contract records
- Link booking transactions to contracts
- Enable dimensional analysis by contract attributes
- Maintain referential integrity

---

## Navigation

- [View Glossary Index](index.md)
- [View Contract Entity](../entities/contract.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Contract  
**Source Attribute**: Contract Key  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
