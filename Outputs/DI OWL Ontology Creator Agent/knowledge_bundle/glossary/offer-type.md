---
title: Offer Type
type: glossary
description: Indicates whether the item is sold as hardware, software subscription, or SaaS subscription
resource: glossary
tags: [glossary, product, offer-type, business-model]
timestamp: 2026-07-28T00:00:00Z
---

# Offer Type

## Business Definition

Indicates whether the item is sold as hardware, software subscription, or SaaS subscription.

---

## Business Meaning

Offer Type classifies products by their delivery and business model. This classification distinguishes between physical hardware, on-premise software subscriptions, and cloud-based SaaS subscriptions. Understanding offer type is critical for revenue recognition, business model analysis, and strategic planning.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_product  
**Source Column**: offer_type  
**Entity**: [Product](../entities/product.md)  
**Attribute**: Offer Type  
**Data Type**: character varying(30)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Product Type
- Delivery Model
- Business Model Type

---

## Related Concepts

### Related Entities
- [Product](../entities/product.md)

### Related Attributes
- [Product Family](product-family.md)
- [Technology Domain](technology-domain.md)

---

## Usage Context

Offer Type is used to:
- Analyze business model mix
- Support revenue recognition
- Track subscription vs hardware sales
- Guide product strategy

---

## Examples

- Hardware
- Software Subscription
- SaaS Subscription

---

## Navigation

- [View Glossary Index](index.md)
- [View Product Entity](../entities/product.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Product  
**Source Attribute**: Offer Type  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
