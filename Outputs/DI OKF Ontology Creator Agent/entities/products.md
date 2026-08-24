---
title: Products
type: entity
description: Products and offers sold to customers with family, technology domain, and offer type attributes
resource: entities
tags: [products, dimension, offerings]
timestamp: 2026-07-28T00:00:00Z
---

# Products

## Business Definition

Stores descriptive information about products and offers sold to customers, including product identity, family, technology domain, offer type, and business entity.

Products represent the goods, services, software, and solutions that are sold through booking transactions.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_product

**Source Columns**: product_key, product_id, product_name, product_family, technology_domain, offer_type, business_entity

---

## Attributes

- **product_key** - Surrogate key that uniquely identifies a product record in the product dimension
- **product_id** - Business identifier or SKU assigned to the product or offer
- **product_name** - Descriptive name of the product or service offering
- **product_family** - Higher-level grouping of related products within the portfolio
- **technology_domain** - Technology area or solution domain the product belongs to
- **offer_type** - Commercial offer classification, such as hardware, software subscription, or SaaS subscription
- **business_entity** - Internal business portfolio or organizational unit associated with the product

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

All booking-related measures can be analyzed by product attributes:
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

## Business Rules

- Each product must have a unique product_key
- product_id serves as the natural business identifier or SKU
- Products are organized hierarchically: product → product_family → technology_domain
- offer_type determines the commercial model (hardware, software, subscription, SaaS)
- Products can be analyzed by family, technology domain, offer type, and business entity

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
