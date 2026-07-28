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

---

## Business Meaning

Partner Tier classifies partners based on their certification level, strategic importance, or investment in the partnership. Tiering reflects partner capabilities, commitment, and performance. Higher-tier partners typically receive enhanced support, better margins, and preferential treatment.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_partner  
**Source Column**: partner_tier  
**Entity**: [Partner](../entities/partner.md)  
**Attribute**: Partner Tier  
**Data Type**: character varying(30)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Partner Level
- Certification Level
- Partner Status

---

## Related Concepts

### Related Entities
- [Partner](../entities/partner.md)

### Related Attributes
- [Partner Key](partner-key.md)
- [Partner Type](partner-type.md)

---

## Usage Context

Partner Tier is used to:
- Classify partners by certification and capability
- Differentiate partner support and benefits
- Analyze performance by partner tier
- Guide partner investment decisions

---

## Examples

- Gold
- Silver
- Bronze
- Premier
- Authorized

---

## Navigation

- [View Glossary Index](index.md)
- [View Partner Entity](../entities/partner.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Partner  
**Source Attribute**: Partner Tier  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
