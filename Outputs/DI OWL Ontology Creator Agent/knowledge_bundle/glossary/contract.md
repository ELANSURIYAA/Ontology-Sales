---
title: Contract
type: glossary
description: Commercial agreements associated with bookings including contract type, term, renewal behavior, and support coverage level
resource: glossary
tags: [glossary, contract, agreement, commercial-terms]
timestamp: 2026-07-28T00:00:00Z
---

# Contract

## Business Definition

Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level.

---

## Business Meaning

A contract represents the formal commercial agreement between the organization and a customer that defines the terms, conditions, duration, pricing structure, and service commitments for products and services. Contracts govern the relationship and establish the framework for booking transactions.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_contract  
**Entity**: [Contract](../entities/contract.md)  
**Confidence Score**: 1.00

---

## Synonyms

- Agreement
- Commercial Agreement
- Service Agreement
- Contract Agreement

---

## Related Concepts

### Related Entities
- [Contract](../entities/contract.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Contract Key](contract-key.md)
- [Contract Type](contract-type.md)
- [Contract Term Months](contract-term-months.md)
- [Auto Renew Flag](auto-renew-flag.md)
- [Coverage Level](coverage-level.md)

### Related Measures
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Usage Context

Contracts are used to:
- Define commercial terms for customer relationships
- Establish pricing and discount structures
- Specify service levels and support coverage
- Set contract duration and renewal terms
- Govern booking transactions

---

## Examples

- SaaS Subscription Contract
- Enterprise Agreement
- Support Contract
- Maintenance Agreement
- Service Level Agreement

---

## Navigation

- [View Glossary Index](index.md)
- [View Contract Entity](../entities/contract.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Entity  
**Source Entity**: Contract  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
