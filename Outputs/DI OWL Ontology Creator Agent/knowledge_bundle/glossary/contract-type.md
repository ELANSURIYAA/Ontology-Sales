---
title: Contract Type
type: glossary
description: Type of commercial agreement attached to the booking such as SaaS subscription, Enterprise Agreement, or support contract
resource: glossary
tags: [glossary, contract, type, classification]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Type

## Business Definition

Describes the type of commercial agreement attached to the booking, such as SaaS subscription, Enterprise Agreement, or support contract.

## Business Meaning

Contract Type classifies the nature and structure of the commercial agreement between the company and customer. Different contract types have different terms, pricing models, and business implications. Understanding contract type distribution is essential for revenue mix analysis and strategic planning.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract  
**Source Column**: contract_type  
**Entity**: [Contract](../entities/contract.md)  
**Attribute**: Contract Type  
**Data Type**: Character Varying(40)  
**Confidence Score**: 1.00

## Synonyms

- Agreement Type
- Contract Classification
- Deal Type

## Related Concepts

- [Contract](./contract.md)
- [Contract Term Months](./contract-term-months.md)
- [Coverage Level](./coverage-level.md)
- [Offer Type](./offer-type.md)

## Usage Context

Contract Type is used to:
- Classify commercial agreements
- Analyze booking mix by contract type
- Track subscription vs perpetual license revenue
- Support contract management and renewal processes

## Example Values

- SaaS Subscription
- Enterprise Agreement
- Support Contract
- Maintenance Agreement
- Professional Services Agreement

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Contract (ENT001)  
**Attribute**: ATTR002
