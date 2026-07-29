---
title: Business Entity
type: glossary
description: Internal business unit or portfolio responsible for the product
resource: glossary
tags: [product, business, entity, organization, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Business Entity

## Business Definition

Internal business unit or portfolio responsible for the product.

---

## Business Meaning

Business Entity identifies the internal organizational unit or business portfolio that owns and manages the product. This classification enables organizational performance tracking and supports internal accountability.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_product  
**Source Column:** business_entity  
**Data Type:** Character Varying(30)  
**Entity:** [Product](../entities/product.md)  
**Attribute:** Business Entity  
**Confidence Score:** 1.00

---

## Related Concepts

- [Product](./product.md) - Parent entity
- [Product Family](./product-family.md) - Portfolio grouping
- [Technology Domain](./technology-domain.md) - Solution domain

---

## Usage Context

Business Entity is used to:
- Identify product ownership and accountability
- Enable business unit performance analysis
- Support organizational reporting
- Track portfolio contribution by business unit

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/product.md)
- [Return to Bundle Index](../index.md)
