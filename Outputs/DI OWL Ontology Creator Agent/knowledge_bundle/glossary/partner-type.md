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

## Business Meaning

Partner Type categorizes partners based on their business model and role in the sales channel. Different partner types have different capabilities, margins, and go-to-market strategies.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_partner  
**Source Column**: partner_type  
**Entity**: [Partner](../entities/partner.md)  
**Attribute**: Partner Type  
**Data Type**: Character Varying(30)  
**Confidence Score**: 1.00

## Synonyms

- Channel Type
- Partner Category
- Partner Classification

## Related Concepts

- [Partner](./partner.md)
- [Partner Tier](./partner-tier.md)
- [Route to Market](./route-to-market.md)

## Usage Context

Partner Type is used to:
- Classify channel partners
- Analyze performance by partner type
- Support channel strategy
- Allocate channel resources

## Example Values

- Distributor
- Reseller
- Systems Integrator
- Managed Service Provider
- Direct

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Partner (ENT005)  
**Attribute**: ATTR028
