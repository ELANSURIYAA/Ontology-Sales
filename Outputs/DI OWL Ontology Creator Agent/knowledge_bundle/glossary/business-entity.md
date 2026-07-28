---
title: Business Entity
type: glossary
description: Internal business unit or portfolio responsible for the product
resource: glossary
tags: [glossary, product, business-entity, organization]
timestamp: 2026-07-28T00:00:00Z
---

# Business Entity

## Business Definition

Internal business unit or portfolio responsible for the product.

---

## Business Meaning

Business Entity identifies the internal organizational unit, business division, or portfolio that owns and manages the product. This classification enables analysis of performance by internal business structure, supports accountability, and guides resource allocation across business units.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_product  
**Source Column**: business_entity  
**Entity**: [Product](../entities/product.md)  
**Attribute**: Business Entity  
**Data Type**: character varying(30)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Business Unit
- Portfolio
- Division
- Product Organization

---

## Related Concepts

### Related Entities
- [Product](../entities/product.md)

### Related Attributes
- [Product Family](product-family.md)
- [Technology Domain](technology-domain.md)

---

## Usage Context

Business Entity is used to:
- Analyze performance by business unit
- Support organizational accountability
- Guide resource allocation
- Enable portfolio management

---

## Navigation

- [View Glossary Index](index.md)
- [View Product Entity](../entities/product.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Product  
**Source Attribute**: Business Entity  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
