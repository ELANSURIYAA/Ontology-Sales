---
title: Contract
type: glossary
description: Commercial agreements associated with bookings including contract type, term, renewal behavior, and support coverage level
resource: glossary
tags: [glossary, contract, agreement, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Contract

## Business Definition

Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level.

## Business Meaning

The Contract represents a formal commercial agreement between the company and a customer that governs the terms, conditions, duration, and support coverage for products and services purchased. Contracts are essential for managing customer commitments, tracking renewal opportunities, and analyzing booking performance by contract characteristics.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract  
**Entity**: [Contract](../entities/contract.md)  
**Attribute**: Entity-level term  
**Confidence Score**: 1.00

## Synonyms

- Agreement
- Commercial Agreement
- Service Agreement
- Subscription Agreement

## Related Concepts

- [Contract Key](./contract-key.md)
- [Contract Type](./contract-type.md)
- [Contract Term Months](./contract-term-months.md)
- [Auto Renew Flag](./auto-renew-flag.md)
- [Coverage Level](./coverage-level.md)
- [Booking Transaction](./booking-transaction.md)
- [Customer](./customer.md)

## Usage Context

Contracts are used to:
- Define commercial terms and conditions
- Track contract duration and renewal dates
- Manage support and service coverage levels
- Analyze booking performance by contract attributes
- Support renewal forecasting and management

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Contract (ENT001)
