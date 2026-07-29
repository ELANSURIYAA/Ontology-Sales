---
title: Contract Key
type: glossary
description: Surrogate key that uniquely identifies a contract record in the contract dimension
resource: glossary
tags: [contract, key, identifier, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Key

## Business Definition

Surrogate key that uniquely identifies a contract record in the contract dimension.

---

## Business Meaning

Contract Key is a system-generated unique identifier used to link contract records to booking transactions. It serves as the primary key for the contract dimension and enables efficient joins in analytical queries.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_contract  
**Source Column:** contract_key  
**Data Type:** Integer  
**Entity:** [Contract](../entities/contract.md)  
**Attribute:** Contract Key  
**Confidence Score:** 1.00

---

## Related Concepts

- [Contract](./contract.md) - Parent entity
- [Booking Transaction](./booking-transaction.md) - Uses contract key as foreign key
- [Contract Type](./contract-type.md) - Contract classification
- [Contract Term Months](./contract-term-months.md) - Contract duration

---

## Usage Context

Contract Key is used to:
- Uniquely identify each contract record
- Link booking transactions to contract attributes
- Enable dimensional analysis by contract characteristics
- Support referential integrity in the data model

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/contract.md)
- [Return to Bundle Index](../index.md)
