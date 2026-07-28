---
title: Coverage Level
type: glossary
description: Level of service or support coverage provided under the contract
resource: glossary
tags: [glossary, contract, coverage, support, service-level]
timestamp: 2026-07-28T00:00:00Z
---

# Coverage Level

## Business Definition

Describes the level of service or support coverage provided under the contract.

---

## Business Meaning

Coverage Level specifies the tier or extent of support and service commitments included in the contract. Different coverage levels typically offer varying response times, support hours, escalation procedures, and service guarantees. Coverage level impacts both customer satisfaction and contract pricing.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_contract  
**Source Column**: coverage_level  
**Entity**: [Contract](../entities/contract.md)  
**Attribute**: Coverage Level  
**Data Type**: character varying(20)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Support Level
- Service Level
- Support Tier
- Coverage Tier

---

## Related Concepts

### Related Entities
- [Contract](../entities/contract.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Contract Key](contract-key.md)
- [Contract Type](contract-type.md)

---

## Usage Context

Coverage Level is used to:
- Define support and service commitments
- Differentiate contract pricing tiers
- Manage customer expectations
- Allocate support resources

---

## Examples

- Basic
- Standard
- Premium
- Enterprise
- 24x7 Support

---

## Navigation

- [View Glossary Index](index.md)
- [View Contract Entity](../entities/contract.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Contract  
**Source Attribute**: Coverage Level  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
