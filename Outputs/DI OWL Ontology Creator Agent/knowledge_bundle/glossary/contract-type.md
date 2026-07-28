---
title: Contract Type
type: glossary
description: Type of commercial agreement attached to the booking such as SaaS subscription, Enterprise Agreement, or support contract
resource: glossary
tags: [glossary, contract, type, agreement-type]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Type

## Business Definition

Describes the type of commercial agreement attached to the booking, such as SaaS subscription, Enterprise Agreement, or support contract.

---

## Business Meaning

Contract Type classifies the nature and structure of the commercial agreement between the organization and the customer. Different contract types have different terms, pricing models, and service commitments that impact revenue recognition and customer relationship management.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_contract  
**Source Column**: contract_type  
**Entity**: [Contract](../entities/contract.md)  
**Attribute**: Contract Type  
**Data Type**: character varying(40)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Agreement Type
- Contract Category
- Contract Classification

---

## Related Concepts

### Related Entities
- [Contract](../entities/contract.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Contract Key](contract-key.md)
- [Contract Term Months](contract-term-months.md)

---

## Usage Context

Contract Type is used to:
- Classify commercial agreements
- Analyze booking performance by contract structure
- Support revenue recognition processes
- Guide contract management workflows

---

## Examples

- SaaS Subscription
- Enterprise Agreement
- Support Contract
- Maintenance Agreement
- Professional Services Agreement

---

## Navigation

- [View Glossary Index](index.md)
- [View Contract Entity](../entities/contract.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Contract  
**Source Attribute**: Contract Type  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
