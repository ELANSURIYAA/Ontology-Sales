---
title: Contract Type
type: glossary
description: Describes the type of commercial agreement attached to the booking
resource: glossary
tags: [contract, type, classification, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Type

## Business Definition

Describes the type of commercial agreement attached to the booking, such as SaaS subscription, Enterprise Agreement, or support contract.

---

## Business Meaning

Contract Type categorizes the commercial structure of agreements, enabling analysis of booking performance by contract model. Different contract types may have different pricing structures, terms, and renewal behaviors.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_contract  
**Source Column:** contract_type  
**Data Type:** Character Varying(40)  
**Entity:** [Contract](../entities/contract.md)  
**Attribute:** Contract Type  
**Confidence Score:** 1.00

---

## Related Concepts

- [Contract](./contract.md) - Parent entity
- [Contract Key](./contract-key.md) - Contract identifier
- [Contract Term Months](./contract-term-months.md) - Contract duration
- [Coverage Level](./coverage-level.md) - Service coverage
- [Booking Transaction](./booking-transaction.md) - Transactions with contract types

---

## Usage Context

Contract Type is used to:
- Classify commercial agreement structures
- Analyze booking performance by contract model
- Support pricing and discount strategies
- Track contract mix and portfolio composition

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/contract.md)
- [Return to Bundle Index](../index.md)
