---
title: Product ID
type: glossary
description: Business identifier or SKU assigned to the product or offer
resource: glossary
tags: [glossary, product, identifier, sku, business-key]
timestamp: 2026-07-28T00:00:00Z
---

# Product ID

## Business Definition

Business identifier or SKU assigned to the product or offer.

---

## Business Meaning

Product ID is the business-recognized identifier or Stock Keeping Unit (SKU) used to uniquely identify products in operational systems, catalogs, and business processes. Unlike the surrogate Product Key, the Product ID is meaningful to business users and is used in product catalogs, ordering systems, and business reporting.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_product

**Source Column**: product_id

**Entity**: [Product](../entities/product.md)

**Attribute**: Product ID

**Data Type**: Character Varying(30)

**Confidence Score**: 1.00

---

## Related Concepts

- [Product](product.md)
- [Product Key](product-key.md)
- [Product Name](product-name.md)

---

## Usage Context

Product ID is used to:
- Identify products in business processes
- Support product lookup and reference
- Enable cross-system product identification
- Facilitate product catalog management
- Support ordering and fulfillment operations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Product](../entities/product.md)
- [Back to Main Index](../index.md)
