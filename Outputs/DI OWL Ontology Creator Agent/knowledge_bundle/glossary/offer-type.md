---
title: Offer Type
type: glossary
description: Indicates whether the item is sold as hardware, software subscription, or SaaS subscription
resource: glossary
tags: [glossary, product, offer-type, subscription, hardware, software]
timestamp: 2026-07-28T00:00:00Z
---

# Offer Type

## Business Definition

Indicates whether the item is sold as hardware, software subscription, or SaaS subscription.

---

## Business Meaning

Offer Type classifies products based on their delivery and consumption model. Common offer types include hardware (physical equipment), software subscription (licensed software with recurring fees), and SaaS subscription (cloud-based software as a service). Offer type classification enables business model analysis, subscription revenue tracking, and strategic shifts from traditional to subscription-based offerings.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_product

**Source Column**: offer_type

**Entity**: [Product](../entities/product.md)

**Attribute**: Offer Type

**Data Type**: Character Varying(30)

**Confidence Score**: 1.00

---

## Related Concepts

- [Product](product.md)
- [Product Key](product-key.md)
- [Product Family](product-family.md)
- [Technology Domain](technology-domain.md)
- [Contract Type](contract-type.md)

---

## Usage Context

Offer Type is used to:
- Classify products by delivery model
- Enable subscription revenue analysis
- Support business model transformation
- Facilitate hardware vs. software analysis
- Enable recurring revenue tracking

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Product](../entities/product.md)
- [Back to Main Index](../index.md)
