---
title: Partner Tier
type: glossary
description: Certification, authorization, or strategic tier assigned to the partner
resource: glossary
tags: [glossary, partner, tier, certification]
timestamp: 2026-07-28T00:00:00Z
---

# Partner Tier

## Business Definition

Indicates the certification, authorization, or strategic tier assigned to the partner.

## Business Meaning

Partner Tier classifies partners based on their certification level, capabilities, and strategic importance. Tier classifications help manage partner programs, allocate support resources, and recognize partner achievements.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_partner  
**Source Column**: partner_tier  
**Entity**: [Partner](../entities/partner.md)  
**Attribute**: Partner Tier  
**Data Type**: Character Varying(30)  
**Confidence Score**: 1.00

## Synonyms

- Partner Level
- Certification Tier
- Partner Status

## Related Concepts

- [Partner](./partner.md)
- [Partner Type](./partner-type.md)

## Usage Context

Partner Tier is used to:
- Classify partner certification levels
- Analyze performance by partner tier
- Manage partner programs
- Allocate partner support

## Example Values

- Gold Partner
- Silver Partner
- Bronze Partner
- Authorized Partner
- Strategic Partner

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Partner (ENT005)  
**Attribute**: ATTR029
