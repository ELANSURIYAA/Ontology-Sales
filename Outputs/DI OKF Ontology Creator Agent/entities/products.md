---
title: Product
type: entity
description: Products and offers sold to customers, including product identity, family, technology domain, offer type, and business entity
resource: entities
tags: [product, offers, portfolio, technology, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Product

## Business Definition

The Product entity stores descriptive information about products and offers sold to customers, including product identity, family, technology domain, offer type, and business entity. This entity enables product portfolio analysis and performance tracking.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_product  
**Source Schema**: quotetobooking  
**Entity Type**: Dimension  
**Grain**: One row per product

---

## Attributes

- product_key
- product_id
- product_name
- product_family
- technology_domain
- offer_type
- business_entity

---

## Primary Keys

- product_key

---

## Foreign Keys

None

---

## Relationships

- [Bookings to Products](../relationships/bookings-to-products.md)

---

## Measures

All booking and revenue measures can be analyzed by product attributes:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Total Quantity](../measures/total-quantity.md)
- [Booking Count](../measures/booking-count.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)

---

## Related Concepts

- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Offer Type](../glossary/offer-type.md)
- [Business Entity](../glossary/business-entity.md)

---

## Business Rules

### Product Identification
Each product is uniquely identified by product_key (surrogate key) and product_id (business key/SKU).

### Product Family Grouping
Products are grouped into product families for higher-level portfolio analysis.

### Technology Domain Classification
Products are classified by technology domain or solution area for market positioning.

### Offer Type Classification
Products are classified by commercial offer type such as hardware, software subscription, or SaaS subscription.

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Products Domain](../domains/products.md)
