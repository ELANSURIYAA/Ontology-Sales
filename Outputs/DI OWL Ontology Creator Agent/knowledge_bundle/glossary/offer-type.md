---
title: Offer Type
type: glossary
description: Indicates whether the item is sold as hardware, software subscription, or SaaS subscription
resource: glossary
tags: [product, offer, type, delivery, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Offer Type

## Business Definition

Indicates whether the item is sold as hardware, software subscription, or SaaS subscription.

---

## Business Meaning

Offer Type categorizes products by their delivery model and consumption pattern. This classification distinguishes between physical hardware, on-premise software subscriptions, and cloud-based SaaS offerings, enabling delivery model analysis.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_product  
**Source Column:** offer_type  
**Data Type:** Character Varying(30)  
**Entity:** [Product](../entities/product.md)  
**Attribute:** Offer Type  
**Confidence Score:** 1.00

---

## Related Concepts

- [Product](./product.md) - Parent entity
- [Product Family](./product-family.md) - Portfolio grouping
- [Technology Domain](./technology-domain.md) - Solution domain

---

## Usage Context

Offer Type is used to:
- Categorize products by delivery model
- Enable offer type-specific analysis
- Support go-to-market strategy
- Track product mix by delivery model

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/product.md)
- [Return to Bundle Index](../index.md)
