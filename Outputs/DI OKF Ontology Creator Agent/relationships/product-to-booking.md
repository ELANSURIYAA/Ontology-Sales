---
title: Product to Booking Relationship
type: relationship
description: Foreign key relationship linking product attributes to booking transactions
resource: relationships
tags: [okf, relationship, product, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Product to Booking Relationship

## Business Description

This relationship links product and offer attributes to individual booking transactions, enabling analysis of bookings by product identity, family, technology domain, offer type, and business entity. Each booking transaction references a specific product through the product foreign key.

---

## Technical Mapping

**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Product Dimension](../entities/product-dimension.md)  
**Attribute**: product_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Fact](../entities/booking-fact.md)  
**Attribute**: product_key  
**Role**: Child (Many side)

---

## Relationship Semantics

- One product can have many booking transactions
- Each booking transaction must reference exactly one product
- The relationship enables product-centric analysis of booking performance
- Product attributes provide context for understanding product portfolio performance

---

## Business Rules

1. Every booking must reference a valid product record
2. Product key in Booking Fact must exist in Product Dimension
3. Product attributes remain consistent for a given product key
4. Referential integrity must be maintained between dimensions and fact

---

## Analytical Use Cases

- Analyze sales performance by product and product family
- Track revenue by technology domain
- Evaluate offer type mix and trends
- Monitor business entity contribution
- Identify product adoption patterns
- Support product strategy and planning

---

## Related Concepts

### Related Domains
- [Product Management](../domains/product-management.md)
- [Sales Transactions](../domains/sales-transactions.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)

---

## Navigation

- [Back to Relationships Index](index.md)
- [Back to Bundle Index](../index.md)
