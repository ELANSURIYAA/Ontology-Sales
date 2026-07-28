---
title: Contract Type
type: glossary
description: Type of commercial agreement attached to the booking
resource: glossary
tags: [glossary, contract, type, agreement]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Type

## Business Definition

Describes the type of commercial agreement attached to the booking, such as SaaS subscription, Enterprise Agreement, or support contract.

---

## Business Meaning

Contract Type classifies the nature of the commercial agreement between the organization and the customer. Different contract types have different terms, pricing models, and business implications. Common types include SaaS subscriptions for cloud services, Enterprise Agreements for large organizational commitments, and support contracts for maintenance and service coverage.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract

**Source Column**: contract_type

**Entity**: [Contract](../entities/contract.md)

**Attribute**: Contract Type

**Data Type**: Character Varying(40)

**Confidence Score**: 1.00

---

## Related Concepts

- [Contract](contract.md)
- [Contract Key](contract-key.md)
- [Offer Type](offer-type.md)
- [Coverage Level](coverage-level.md)

---

## Usage Context

Contract Type is used to:
- Classify commercial agreements
- Analyze revenue by contract model
- Support contract lifecycle management
- Enable contract type-specific reporting
- Facilitate pricing and terms analysis

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Contract](../entities/contract.md)
- [Back to Main Index](../index.md)
