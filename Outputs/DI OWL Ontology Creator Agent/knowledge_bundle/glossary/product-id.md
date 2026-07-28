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

Product ID is the business-level identifier or Stock Keeping Unit (SKU) used to reference products in operational systems, catalogs, and business communications. Unlike the surrogate Product Key, the Product ID is a meaningful business identifier used in product management and ordering systems.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_product  
**Source Column**: product_id  
**Entity**: [Product](../entities/product.md)  
**Attribute**: Product ID  
**Data Type**: character varying(30)  
**Nullable**: No  
**Confidence Score**: 1.00

---

## Synonyms

- SKU
- Product Number
- Product Code
- Part Number

---

## Related Concepts

### Related Entities
- [Product](../entities/product.md)

### Related Attributes
- [Product Key](product-key.md)
- [Product Name](product-name.md)

---

## Usage Context

Product ID is used to:
- Identify products in business operations
- Reference products in orders and catalogs
- Link product data across systems

---

## Navigation

- [View Glossary Index](index.md)
- [View Product Entity](../entities/product.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Product  
**Source Attribute**: Product ID  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
