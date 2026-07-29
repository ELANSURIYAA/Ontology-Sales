---
title: Coverage Level
type: glossary
description: Level of service or support coverage provided under the contract
resource: glossary
tags: [glossary, contract, coverage, support, service]
timestamp: 2026-07-28T00:00:00Z
---

# Coverage Level

## Business Definition

Describes the level of service or support coverage provided under the contract.

## Business Meaning

Coverage Level defines the tier or extent of support and service that the customer receives as part of their contract. Different coverage levels typically include varying response times, support hours, and service features. Coverage level impacts pricing, customer satisfaction, and renewal rates.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract  
**Source Column**: coverage_level  
**Entity**: [Contract](../entities/contract.md)  
**Attribute**: Coverage Level  
**Data Type**: Character Varying(20)  
**Confidence Score**: 1.00

## Synonyms

- Support Level
- Service Tier
- Support Tier
- Service Level

## Related Concepts

- [Contract](./contract.md)
- [Contract Type](./contract-type.md)
- [Customer](./customer.md)
- [Account Tier](./account-tier.md)

## Usage Context

Coverage Level is used to:
- Define support and service entitlements
- Differentiate premium vs standard support offerings
- Analyze booking performance by coverage level
- Support pricing and packaging strategies

## Example Values

- Premium Support
- Standard Support
- Basic Support
- 24x7 Support
- Business Hours Support

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Contract (ENT001)  
**Attribute**: ATTR005
