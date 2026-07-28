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

Contract Key is a system-generated unique identifier used to establish relationships between the contract dimension and booking transaction fact records. It serves as the primary key for contract records and enables efficient data integration and referential integrity.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract

**Source Column**: contract_key

**Entity**: [Contract](../entities/contract.md)

**Attribute**: Contract Key

**Data Type**: Integer

**Confidence Score**: 1.00

---

## Related Concepts

- [Contract](contract.md)
- [Booking Transaction](booking-transaction.md)

---

## Usage Context

Contract Key is used to:
- Uniquely identify contract records
- Link booking transactions to contracts
- Maintain referential integrity
- Enable efficient joins between fact and dimension tables
- Support data warehouse operations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Contract](../entities/contract.md)
- [Back to Main Index](../index.md)
