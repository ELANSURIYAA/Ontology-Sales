---
title: Product Key
type: glossary
description: Surrogate key that uniquely identifies a product record in the product dimension
resource: glossary
tags: [glossary, product, key, identifier, surrogate-key]
timestamp: 2026-07-28T00:00:00Z
---

# Product Key

## Business Definition

Surrogate key that uniquely identifies a product record in the product dimension.

---

## Business Meaning

Product Key is a system-generated unique identifier used to link product records to booking transactions. It serves as the primary key for the product dimension and enables efficient joins and referential integrity in the data model.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_product  
**Source Column**: product_key  
**Entity**: [Product](../entities/product.md)  
**Attribute**: Product Key  
**Data Type**: integer  
**Nullable**: No  
**Primary Key**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Product Identifier
- Product Surrogate Key

---

## Related Concepts

### Related Entities
- [Product](../entities/product.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Relationships
- [Product to Booking Transaction](../relationships/product-to-booking-transaction.md)

---

## Usage Context

Product Key is used to:
- Uniquely identify product records
- Link booking transactions to products
- Enable dimensional analysis by product attributes
- Maintain referential integrity

---

## Navigation

- [View Glossary Index](index.md)
- [View Product Entity](../entities/product.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Product  
**Source Attribute**: Product Key  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
