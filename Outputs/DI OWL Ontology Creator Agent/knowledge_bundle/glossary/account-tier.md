---
title: Account Tier
type: glossary
description: Strategic importance or service tier of the customer account
resource: glossary
tags: [glossary, customer, account-tier, strategic-importance]
timestamp: 2026-07-28T00:00:00Z
---

# Account Tier

## Business Definition

Indicates the strategic importance or service tier of the customer account.

---

## Business Meaning

Account Tier classifies customers based on their strategic value, revenue potential, or service level. Tiering enables prioritization of sales and support resources, differentiated service delivery, and strategic account management. Higher-tier accounts typically receive enhanced support and dedicated resources.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_customer  
**Source Column**: account_tier  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Account Tier  
**Data Type**: character varying(20)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Customer Tier
- Account Level
- Strategic Tier
- Service Tier

---

## Related Concepts

### Related Entities
- [Customer](../entities/customer.md)

### Related Attributes
- [Customer Segment](customer-segment.md)
- [Customer Key](customer-key.md)

---

## Usage Context

Account Tier is used to:
- Prioritize sales and support resources
- Differentiate service levels
- Analyze performance by account importance
- Guide account management strategies

---

## Examples

- Strategic
- Tier 1
- Tier 2
- Standard
- Premium

---

## Navigation

- [View Glossary Index](index.md)
- [View Customer Entity](../entities/customer.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Customer  
**Source Attribute**: Account Tier  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
