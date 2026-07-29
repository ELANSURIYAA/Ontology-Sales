---
title: Contract
type: glossary
description: Stores the business attributes of commercial agreements associated with bookings
resource: glossary
tags: [contract, agreement, commercial, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Contract

## Business Definition

Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level.

---

## Business Meaning

A contract represents a formal commercial agreement between the vendor and customer that defines the terms, conditions, duration, and coverage level for products and services. Contracts govern the relationship and establish the framework for booking transactions.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_contract  
**Entity:** [Contract](../entities/contract.md)  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Transactions governed by contracts
- [Contract Key](./contract-key.md) - Unique identifier for contracts
- [Contract Type](./contract-type.md) - Type of commercial agreement
- [Contract Term Months](./contract-term-months.md) - Duration of contract
- [Auto Renew Flag](./auto-renew-flag.md) - Renewal behavior
- [Coverage Level](./coverage-level.md) - Service coverage provided
- [Annual Contract Value USD](./annual-contract-value-usd.md) - Annual value metric
- [Total Contract Value USD](./total-contract-value-usd.md) - Total value metric

---

## Usage Context

Contracts are used to:
- Define commercial terms for customer engagements
- Establish pricing and discount structures
- Specify service levels and support coverage
- Govern renewal and termination conditions
- Track multi-year commitments and obligations

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/contract.md)
- [Return to Bundle Index](../index.md)
