---
title: Account Tier
type: glossary
description: Strategic importance or service tier of the customer account
resource: glossary
tags: [glossary, customer, tier, classification]
timestamp: 2026-07-28T00:00:00Z
---

# Account Tier

## Business Definition

Indicates the strategic importance or service tier of the customer account.

## Business Meaning

Account Tier classifies customers based on their strategic value, revenue potential, or service level. Tier classifications help prioritize account management resources, customize service levels, and focus on high-value relationships.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer  
**Source Column**: account_tier  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Account Tier  
**Data Type**: Character Varying(20)  
**Confidence Score**: 1.00

## Synonyms

- Customer Tier
- Account Classification
- Strategic Tier

## Related Concepts

- [Customer](./customer.md)
- [Customer Segment](./customer-segment.md)
- [Coverage Level](./coverage-level.md)

## Usage Context

Account Tier is used to:
- Prioritize account management activities
- Allocate sales and support resources
- Customize service levels and engagement models
- Analyze performance by account importance

## Example Values

- Strategic
- Tier 1
- Tier 2
- Tier 3
- Key Account

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Customer (ENT002)  
**Attribute**: ATTR011
