---
title: Partner Type
type: glossary
description: Classification of partner by operating model such as distributor, reseller, systems integrator, or direct
resource: glossary
tags: [glossary, partner, type, classification]
timestamp: 2026-07-28T00:00:00Z
---

# Partner Type

## Business Definition

Classifies the partner by operating model, such as distributor, reseller, systems integrator, or direct.

---

## Business Meaning

Partner Type categorizes partners based on their business model and role in the sales process. Different partner types have distinct capabilities, market coverage, and value propositions. This classification enables targeted partner strategies and channel performance analysis.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_partner  
**Source Column**: partner_type  
**Entity**: [Partner](../entities/partner.md)  
**Attribute**: Partner Type  
**Data Type**: character varying(30)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Channel Type
- Partner Category
- Partner Classification

---

## Related Concepts

### Related Entities
- [Partner](../entities/partner.md)

### Related Attributes
- [Partner Key](partner-key.md)
- [Partner Tier](partner-tier.md)
- [Route to Market](route-to-market.md)

---

## Usage Context

Partner Type is used to:
- Classify partners by business model
- Analyze channel performance
- Guide partner strategies
- Support channel planning

---

## Examples

- Distributor
- Reseller
- Systems Integrator
- Direct
- Value-Added Reseller

---

## Navigation

- [View Glossary Index](index.md)
- [View Partner Entity](../entities/partner.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Partner  
**Source Attribute**: Partner Type  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
