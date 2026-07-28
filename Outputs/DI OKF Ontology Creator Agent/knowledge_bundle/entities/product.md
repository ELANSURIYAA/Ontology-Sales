---
title: Product
type: entity
description: Business entity representing products and offers sold to customers.
resource: entities
tags: [entity, product, offer, sales]
timestamp: 2026-07-28
---

# Product

## Business Definition
Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity.

## Technical Mapping
- Source Table: `QuoteToBooking.dim_product`
- Related Glossary: [Product](../glossary/product.md)

## Attributes
- Product Key
- Product ID
- Product Name
- Product Family
- Technology Domain
- Offer Type
- Business Entity

## Primary Keys
- Product Key

## Foreign Keys
None

## Measures
None

## Relationships
- [Product to Booking Transaction](../relationships/product-to-booking-transaction.md)

## Related Concepts
- [Product ID](../glossary/product-id.md)
- [Product Name](../glossary/product-name.md)
- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Offer Type](../glossary/offer-type.md)
- [Business Entity](../glossary/business-entity.md)
- [Booking Transaction](booking-transaction.md)
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

## Business Rules
- Each product record is uniquely identified by Product Key.
- Product ID is the business identifier or SKU assigned to the product or offer.
- A product may be associated with multiple booking transactions.
