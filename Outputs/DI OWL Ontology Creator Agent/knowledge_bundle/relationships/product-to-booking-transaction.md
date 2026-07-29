---
title: Product to Booking Transaction
type: relationship
description: One-to-Many relationship linking products to booking transactions
resource: relationships
tags: [relationship, product, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Product to Booking Transaction

## Business Description

This relationship links Product dimension records to Booking Transaction fact records. Each product can be associated with multiple booking transactions, while each booking transaction involves exactly one product. This relationship enables product portfolio analysis of booking performance across product families, technology domains, and offer types.

---

## Relationship Details

**Relationship ID**: REL006  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Product](../entities/product.md)  
**Entity ID**: ENT006  
**Attribute**: Product Key  
**Technical Column**: product_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Entity ID**: ENT008  
**Attribute**: Product Key  
**Technical Column**: product_key  
**Role**: Child (Many side)

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_product  
**Target Table**: QuoteToBooking.fact_bookings  
**Join Condition**: `dim_product.product_key = fact_bookings.product_key`

---

## Business Rules

1. Each booking transaction must reference a valid product
2. A product can have zero or many booking transactions
3. Product Key in Booking Transaction must exist in Product dimension
4. Referential integrity must be maintained
5. Product attributes apply to all associated booking transactions

---

## Analytical Usage

This relationship enables analysis of:

- Product portfolio performance and revenue contribution
- Product family booking trends and growth
- Technology domain adoption and market penetration
- Offer type mix (hardware, software subscription, SaaS)
- Business entity performance and product ownership

---

## Related Concepts

- [Product](../entities/product.md) - Source dimension entity
- [Booking Transaction](../entities/booking-transaction.md) - Target fact entity
- [Customer](../entities/customer.md) - Customers purchasing products
- [Contract](../entities/contract.md) - Product subscription agreements
- [Partner](../entities/partner.md) - Partners selling products

---

## Semantic Links

- [Relationship Index](./index.md)
- [Entity Index](../entities/index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Main Index](../index.md)

---

## Metadata

**Relationship ID**: REL006  
**Source Entity ID**: ENT006  
**Target Entity ID**: ENT008  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
