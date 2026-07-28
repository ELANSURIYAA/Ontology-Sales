---
title: Product
type: entity
description: Products and offers sold to customers including product family, technology domain, offer type, and business entity
resource: entities
tags: [entity, dimension, product, offer, sku, portfolio]
timestamp: 2026-07-28T00:00:00Z
---

# Product

## Business Definition

Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_product

**Source System**: QuoteToBooking

**Entity Type**: Dimension

---

## Attributes

- **Product Key** (product_key): Surrogate key that uniquely identifies a product record in the product dimension
- **Product ID** (product_id): Business identifier or SKU assigned to the product or offer
- **Product Name** (product_name): Commercial name of the product or subscription offer sold to the customer
- **Product Family** (product_family): Higher-level product grouping used for portfolio and performance analysis
- **Technology Domain** (technology_domain): Technology area or solution domain to which the product belongs
- **Offer Type** (offer_type): Indicates whether the item is sold as hardware, software subscription, or SaaS subscription
- **Business Entity** (business_entity): Internal business unit or portfolio responsible for the product

---

## Primary Keys

- **Product Key** (product_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- **[Product to Booking Transaction](../relationships/product-to-booking-transaction.md)**: One-to-Many relationship linking products to booking transactions

### Related Entities

- [Booking Transaction](booking-transaction.md): Fact entity that references this dimension
- [Customer](customer.md): Related through product purchases
- [Partner](partner.md): Related through product sales

---

## Measures

This dimension supports analysis of the following measures:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Concepts

- [Product](../glossary/product.md)
- [Product Key](../glossary/product-key.md)
- [Product ID](../glossary/product-id.md)
- [Product Name](../glossary/product-name.md)
- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Offer Type](../glossary/offer-type.md)
- [Business Entity](../glossary/business-entity.md)

---

## Business Rules

1. Product Key is a surrogate key and must be unique
2. Product ID is the business identifier or SKU for the product
3. Product Name is the commercial name of the product or offer
4. Product Family groups products for portfolio analysis
5. Technology Domain identifies the solution area (e.g., networking, security, collaboration, observability)
6. Offer Type classifies products as hardware, software subscription, or SaaS subscription
7. Business Entity identifies the responsible business unit or portfolio
8. Every booking transaction must reference a valid product
9. Product attributes support portfolio and product mix analysis

---

## Usage Examples

**Analysis by Product Family**:
- Compare booking revenue across product families
- Analyze product family growth trends
- Measure product family contribution to total revenue

**Analysis by Technology Domain**:
- Evaluate performance by solution domain (networking, security, collaboration, observability)
- Analyze technology domain adoption by customer segment
- Compare technology domain growth rates

**Analysis by Offer Type**:
- Compare hardware vs. software subscription vs. SaaS subscription revenue
- Analyze subscription adoption trends
- Measure offer type mix by customer segment

**Analysis by Business Entity**:
- Evaluate business unit performance
- Analyze portfolio contribution to revenue
- Compare business entity growth rates

**Product Performance**:
- Identify top-performing products by booking revenue
- Analyze product adoption by geography
- Compare discount rates by product family

**Product Mix Analysis**:
- Evaluate product portfolio balance
- Analyze cross-sell and upsell opportunities
- Measure product diversification by customer

---

## Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Main Index](../index.md)
- [View Relationships](../relationships/index.md)
- [View Measures](../measures/index.md)
- [View Glossary](../glossary/index.md)
