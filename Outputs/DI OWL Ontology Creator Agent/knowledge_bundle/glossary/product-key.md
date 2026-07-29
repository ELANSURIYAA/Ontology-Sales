---
title: Product Key
type: glossary
description: Surrogate key that uniquely identifies a product record in the product dimension
resource: glossary
tags: [product, key, identifier, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Product Key

## Business Definition

Surrogate key that uniquely identifies a product record in the product dimension.

---

## Business Meaning

Product Key is a system-generated unique identifier used to link product records to booking transactions. It serves as the primary key for the product dimension and enables efficient joins in analytical queries.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_product  
**Source Column:** product_key  
**Data Type:** Integer  
**Entity:** [Product](../entities/product.md)  
**Attribute:** Product Key  
**Confidence Score:** 1.00

---

## Related Concepts

- [Product](./product.md) - Parent entity
- [Booking Transaction](./booking-transaction.md) - Uses product key as foreign key
- [Product ID](./product-id.md) - Business identifier

---

## Usage Context

Product Key is used to:
- Uniquely identify each product record
- Link booking transactions to product attributes
- Enable dimensional analysis by product characteristics
- Support referential integrity in the data model

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/product.md)
- [Return to Bundle Index](../index.md)
