---
title: Product Key
type: glossary
description: Surrogate key that uniquely identifies a product record in the product dimension
resource: glossary
tags: [okf, glossary, attribute, product, key]
timestamp: 2026-07-28T00:00:00Z
---

# Product Key

## Business Definition

Surrogate key that uniquely identifies a product record in the product dimension.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_product  
**Source Column**: product_key  
**Entity**: Product Dimension  
**Attribute**: Product Key

---

## Business Meaning

The Product Key is a system-generated unique identifier used to link booking transactions to their associated product attributes. It serves as the primary key in the Product Dimension and as a foreign key in the Booking Fact table.

---

## Related Concepts

- [Product Dimension](product-dimension.md)
- [Booking Fact](booking-fact.md)

---

## Navigation

- [Back to Glossary Index](index.md)
- [Back to Bundle Index](../index.md)
