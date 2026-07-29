---
title: Route to Market
type: glossary
description: Sales delivery path through which the product or service reached the customer
resource: glossary
tags: [glossary, partner, route, channel]
timestamp: 2026-07-28T00:00:00Z
---

# Route to Market

## Business Definition

Describes the sales delivery path through which the product or service reached the customer.

## Business Meaning

Route to Market defines the channel path from vendor to customer, including direct sales and various indirect channel models. Understanding route to market is essential for channel strategy, margin analysis, and go-to-market optimization.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_partner  
**Source Column**: route_to_market  
**Entity**: [Partner](../entities/partner.md)  
**Attribute**: Route to Market  
**Data Type**: Character Varying(20)  
**Confidence Score**: 1.00

## Synonyms

- Channel Route
- Sales Channel
- Go-to-Market Route

## Related Concepts

- [Partner](./partner.md)
- [Partner Type](./partner-type.md)
- [Partner Tier](./partner-tier.md)

## Usage Context

Route to Market is used to:
- Analyze channel effectiveness
- Compare direct vs indirect performance
- Optimize go-to-market strategy
- Support channel planning

## Example Values

- Direct
- One-Tier (Direct to Partner to Customer)
- Two-Tier (Direct to Distributor to Reseller to Customer)

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Partner (ENT005)  
**Attribute**: ATTR030
