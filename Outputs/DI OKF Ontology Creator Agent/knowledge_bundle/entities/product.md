---
title: Product
type: entity
description: Business entity describing products and offers sold to customers.
resource: entities
tags: product,entity,portfolio,sales
timestamp: 2026-07-28T00:00:00Z
---

# Product

## Business Definition

Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity.

---

## Technical Mapping

- Source Table: `QuoteToBooking.dim_product`
- Domain: [Sales Bookings and Revenue Analytics](../domains/sales_bookings_and_revenue_analytics.md)

---

## Attributes

- Product Key (`product_key`) - integer - not nullable
- Product ID (`product_id`) - character varying(30) - not nullable
- Product Name (`product_name`) - character varying(80)
- Product Family (`product_family`) - character varying(30)
- Technology Domain (`technology_domain`) - character varying(40)
- Offer Type (`offer_type`) - character varying(30)
- Business Entity (`business_entity`) - character varying(30)

---

## Primary Keys

- Product Key

---

## Foreign Keys

None

---

## Measures

None

---

## Relationships

- [Product to Booking Transaction](../relationships/product_to_booking_transaction.md)

---

## Related Concepts

- [Product](../glossary/product.md)
- [Product ID](../glossary/product_id.md)
- [Product Name](../glossary/product_name.md)
- [Product Family](../glossary/product_family.md)
- [Technology Domain](../glossary/technology_domain.md)
- [Offer Type](../glossary/offer_type.md)
- [Business Entity](../glossary/business_entity.md)

---

## Business Rules

- Each product record is uniquely identified by Product Key.
- Product ID is the business identifier or SKU assigned to the product or offer.
- A product can be associated with multiple booking transactions.

---

## Semantic Cross Links

- [Entities Index](index.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Booking Transaction](booking_transaction.md)
- [Product to Booking Transaction](../relationships/product_to_booking_transaction.md)
- [Glossary: Product](../glossary/product.md)
