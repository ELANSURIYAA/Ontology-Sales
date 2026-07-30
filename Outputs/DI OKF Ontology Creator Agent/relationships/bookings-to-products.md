---
title: Bookings to Products
type: relationship
description: Links booking transactions to the product or offer that was sold
resource: relationships
tags: [bookings, products, relationship, many-to-one]
timestamp: 2024-01-15T00:00:00Z
---

# Bookings to Products

## Business Definition

This relationship links booking transactions to the product or offer that was sold, enabling analysis of bookings by product family, technology domain, offer type, and business entity.

---

## Relationship Details

**Source Entity**: [Booking Transaction](../entities/bookings.md)  
**Target Entity**: [Product](../entities/products.md)  
**Relationship Type**: Many-to-One  
**Cardinality**: Many bookings can be associated with one product

---

## Technical Mapping

**Join Type**: Inner Join  
**Left Key**: bookings.product_key  
**Right Key**: products.product_key

---

## Business Description

Each booking transaction is associated with a specific product or offer that was sold. Product attributes include product family (higher-level grouping), technology domain (solution area), offer type (hardware, software subscription, SaaS subscription), and business entity (internal portfolio unit). Multiple booking transactions can be associated with the same product.

---

## Usage

This relationship enables analysis such as:

- Product portfolio performance
- Product family trends
- Technology domain analysis
- Offer type mix (hardware vs software vs SaaS)
- Business entity contribution

---

## Related Concepts

- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Offer Type](../glossary/offer-type.md)
- [Business Entity](../glossary/business-entity.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Product Entity](../entities/products.md)
- [View Products Domain](../domains/products.md)
