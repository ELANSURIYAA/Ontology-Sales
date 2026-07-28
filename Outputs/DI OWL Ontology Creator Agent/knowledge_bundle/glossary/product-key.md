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

Product Key is a system-generated unique identifier used to establish relationships between the product dimension and booking transaction fact records. It serves as the primary key for product records and enables efficient data integration and referential integrity.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_product

**Source Column**: product_key

**Entity**: [Product](../entities/product.md)

**Attribute**: Product Key

**Data Type**: Integer

**Confidence Score**: 1.00

---

## Related Concepts

- [Product](product.md)
- [Booking Transaction](booking-transaction.md)

---

## Usage Context

Product Key is used to:
- Uniquely identify product records
- Link booking transactions to products
- Maintain referential integrity
- Enable efficient joins between fact and dimension tables
- Support data warehouse operations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Product](../entities/product.md)
- [Back to Main Index](../index.md)
