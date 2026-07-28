---
title: Route to Market
type: glossary
description: Sales delivery path through which the product or service reached the customer
resource: glossary
tags: [glossary, partner, route-to-market, channel]
timestamp: 2026-07-28T00:00:00Z
---

# Route to Market

## Business Definition

Describes the sales delivery path through which the product or service reached the customer.

---

## Business Meaning

Route to Market identifies the channel or path used to deliver products and services to customers. It describes whether sales occur through direct sales, channel partners, distributors, or other delivery mechanisms. Understanding route to market enables channel strategy optimization and market coverage analysis.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_partner  
**Source Column**: route_to_market  
**Entity**: [Partner](../entities/partner.md)  
**Attribute**: Route to Market  
**Data Type**: character varying(20)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Channel
- Sales Channel
- Distribution Channel
- Go-to-Market Path

---

## Related Concepts

### Related Entities
- [Partner](../entities/partner.md)

### Related Attributes
- [Partner Type](partner-type.md)
- [Partner Tier](partner-tier.md)

---

## Usage Context

Route to Market is used to:
- Analyze channel effectiveness
- Optimize go-to-market strategies
- Track sales by delivery path
- Guide channel investment decisions

---

## Examples

- Direct
- Channel
- Two-Tier
- Online

---

## Navigation

- [View Glossary Index](index.md)
- [View Partner Entity](../entities/partner.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Partner  
**Source Attribute**: Route to Market  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
