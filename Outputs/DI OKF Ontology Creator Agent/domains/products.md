---
title: Products Domain
type: domain
description: Products and offers sold to customers, including product identity, family, technology domain, offer type, and business entity
resource: domains
tags: [products, offers, portfolio, technology, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Products Domain

## Business Definition

The Products domain stores descriptive information about products and offers sold to customers, including product identity, family, technology domain, offer type, and business entity. This domain enables product portfolio analysis and performance tracking.

---

## Business Purpose

The Products domain enables analysis of:

- Product portfolio performance
- Product family and technology domain trends
- Offer type mix (hardware, software, SaaS)
- Business entity contribution
- Product-level revenue and booking performance
- Cross-sell and product adoption patterns

---

## Domain Type

**Dimension Domain** - Descriptive attributes for product analysis

---

## Related Entities

- [Product](../entities/products.md)

---

## Related Measures

All booking and revenue measures can be analyzed by product attributes:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Total Quantity](../measures/total-quantity.md)
- [Booking Count](../measures/booking-count.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)

---

## Related Relationships

- [Bookings to Products](../relationships/bookings-to-products.md)

---

## Key Concepts

### Product Family
Higher-level grouping of related products within the portfolio for strategic analysis.

### Technology Domain
Technology area or solution domain the product belongs to for market positioning.

### Offer Type
Commercial offer classification such as hardware, software subscription, or SaaS subscription.

### Business Entity
Internal business portfolio or organizational unit associated with the product.

---

## Semantic Links

### Related Domains
- [Bookings Domain](bookings.md) - Product sales
- [Customers Domain](customers.md) - Product buyers

### Related Glossary
- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Offer Type](../glossary/offer-type.md)
- [Business Entity](../glossary/business-entity.md)

---

## Technical Mapping

**Source Table**: quotetobooking.dim_product  
**Primary Key**: product_key  
**Business Key**: product_id

---

## Navigation

- [Return to Domains Index](index.md)
- [Return to Main Index](../index.md)
- [View Product Entity](../entities/products.md)
