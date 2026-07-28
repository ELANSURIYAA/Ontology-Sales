---
title: Product
type: entity
description: Business entity representing products and offers sold to customers
resource: entities
tags: [entity, dimension, product, offer, portfolio, sku]
timestamp: 2026-07-28T00:00:00Z
---

# Product

## Business Definition

Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity. The Product entity enables analysis of product portfolio performance, technology domain effectiveness, and offer type strategies.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_product  
**Entity Type**: Dimension  
**Entity ID**: ENT006

---

## Attributes

- **Product Key** (product_key) - integer, NOT NULL
- **Product ID** (product_id) - character varying(30), NOT NULL
- **Product Name** (product_name) - character varying(80), NULL
- **Product Family** (product_family) - character varying(30), NULL
- **Technology Domain** (technology_domain) - character varying(40), NULL
- **Offer Type** (offer_type) - character varying(30), NULL
- **Business Entity** (business_entity) - character varying(30), NULL

---

## Primary Keys

- **Product Key** (product_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- [Product to Booking Transaction](../relationships/product-to-booking-transaction.md) - Links products to booking transactions (One-to-Many)

---

## Measures

Products are analyzed using measures from related booking transactions:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Concepts

### Related Entities
- [Booking Transaction](booking-transaction.md) - Booking transactions for this product
- [Customer](customer.md) - Customers purchasing products
- [Contract](contract.md) - Contracts covering products

### Related Glossary Terms
- [Product](../glossary/product.md)
- [Product Key](../glossary/product-key.md)
- [Product ID](../glossary/product-id.md)
- [Product Name](../glossary/product-name.md)
- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Offer Type](../glossary/offer-type.md)
- [Business Entity](../glossary/business-entity.md)

### Related Domains
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Uniqueness**: Each product record is uniquely identified by Product Key
2. **Business Identifier**: Product ID serves as the business identifier or SKU for the product
3. **Product Hierarchy**: Products are organized into Product Families for portfolio analysis
4. **Technology Classification**: Technology Domain identifies the solution area (networking, security, collaboration, observability)
5. **Offer Classification**: Offer Type indicates whether the product is hardware, software subscription, or SaaS subscription
6. **Business Ownership**: Business Entity identifies the internal business unit or portfolio responsible for the product

---

## Usage Examples

### Product Portfolio Analysis
Analyze booking amounts by product family to understand which product lines drive the most revenue.

### Technology Domain Analysis
Evaluate booking performance by technology domain (networking, security, collaboration, observability) to assess solution area effectiveness.

### Offer Type Analysis
Compare booking amounts across offer types (hardware, software subscription, SaaS subscription) to understand business model mix.

### Product Performance
Identify top-performing products by booking amount and quantity sold to optimize product strategy and resource allocation.

### Business Entity Analysis
Analyze booking performance by business entity to assess internal portfolio performance and accountability.

---

## Data Quality Notes

- Product Key is mandatory and serves as the primary key
- Product ID is mandatory and serves as the business identifier (SKU)
- Product Name should be populated for all active product records
- Product Family, Technology Domain, Offer Type, and Business Entity classifications support portfolio analysis
- NULL values in descriptive attributes may indicate incomplete product profiles
- Product dimension should include all sellable products and offers

---

## Navigation

- [View Entity Index](index.md)
- [View Related Relationships](../relationships/index.md)
- [View Related Measures](../measures/index.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Entity ID**: ENT006  
**Domain**: Sales Bookings and Revenue Analytics  
**Entity Type**: Dimension  
**Attribute Count**: 7  
**Relationship Count**: 1  
**Last Updated**: 2026-07-28T00:00:00Z
