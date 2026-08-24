---
title: Bookings to Products
type: relationship
description: Links booking transactions to products and offers
resource: relationships
tags: [bookings, products, relationship, many-to-one]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Products

## Business Definition

Links booking transactions to products and offers sold to customers, including product identity, family, technology domain, offer type, and business entity.

This relationship enables analysis of product performance and supports product portfolio optimization and technology domain analysis.

---

## Relationship Type

**many-to-one**

Multiple booking transactions can be associated with the same product.

---

## Source Entity

[Bookings](../entities/bookings.md)

---

## Target Entity

[Products](../entities/products.md)

---

## Cardinality

- Each booking transaction must be associated with exactly one product record
- Each product record can be associated with multiple booking transactions

---

## Technical Mapping

**Join Condition**: bookings.product_key = products.product_key

**Left Dataset**: bookings (quotetobooking.fact_bookings)

**Right Dataset**: products (quotetobooking.dim_product)

**Join Keys**:
- Left: product_key
- Right: product_key

---

## Business Purpose

This relationship enables:
- Product performance and profitability analysis
- Product family and portfolio analysis
- Technology domain revenue analysis
- Offer type analysis (hardware, software subscription, SaaS)
- Business entity and organizational unit analysis
- Product mix and cross-sell analysis

---

## Related Measures

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total Quantity](../measures/total-quantity.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)
- [Booking Count](../measures/booking-count.md)

---

## Related Concepts

- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
