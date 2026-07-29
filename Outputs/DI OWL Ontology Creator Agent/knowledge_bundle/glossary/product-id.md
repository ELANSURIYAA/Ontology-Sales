---
title: Product ID
type: glossary
description: Business identifier or SKU assigned to the product or offer
resource: glossary
tags: [product, identifier, sku, business-key, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Product ID

## Business Definition

Business identifier or SKU assigned to the product or offer.

---

## Business Meaning

Product ID is the business-recognized identifier or stock keeping unit (SKU) used to reference products in operational systems and business communications. Unlike the surrogate Product Key, this is a meaningful business identifier.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_product  
**Source Column:** product_id  
**Data Type:** Character Varying(30)  
**Entity:** [Product](../entities/product.md)  
**Attribute:** Product ID  
**Confidence Score:** 1.00

---

## Related Concepts

- [Product](./product.md) - Parent entity
- [Product Key](./product-key.md) - Surrogate identifier
- [Product Name](./product-name.md) - Commercial name

---

## Usage Context

Product ID is used to:
- Reference products in business processes
- Integrate with operational systems
- Support product lookup and identification
- Enable cross-system product tracking

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/product.md)
- [Return to Bundle Index](../index.md)
