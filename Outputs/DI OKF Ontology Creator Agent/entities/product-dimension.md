---
title: Product Dimension
type: entity
description: Product and offer attributes used to analyze bookings by product identity, family, and technology domain
resource: entities
tags: [okf, entity, product, dimension, portfolio]
timestamp: 2026-07-28T00:00:00Z
---

# Product Dimension

## Business Definition

The Product Dimension stores product and offer attributes used to analyze bookings by product identity, family, technology domain, offer type, and business entity. This dimension enables product portfolio analytics and supports product strategy and planning.

---

## Technical Mapping

**Source Schema**: quotetobooking  
**Source Table**: dim_product  
**Entity Type**: Dimension  
**Grain**: One record per unique product

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

None (this is a dimension table)

---

## Relationships

### Outbound Relationships
- [Product to Booking](../relationships/product-to-booking.md) - One-to-Many relationship to Booking Fact

---

## Measures

All booking measures can be analyzed by product attributes:

- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Related Concepts

### Related Entities
- [Booking Fact](booking-fact.md)

### Related Domains
- [Product Management](../domains/product-management.md)
- [Sales Transactions](../domains/sales-transactions.md)
- [Pricing](../domains/pricing.md)

### Related Glossary Terms
- [Product Dimension](../glossary/product-dimension.md)
- [Product Key](../glossary/product-key.md)
- [Product ID](../glossary/product-id.md)
- [Product Name](../glossary/product-name.md)
- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Offer Type](../glossary/offer-type.md)
- [Business Entity](../glossary/business-entity.md)

---

## Business Rules

1. Product Key must be unique and not null
2. Product ID must be unique and not null
3. Product Name is required for all records
4. Product Family should be populated for all products
5. Technology Domain should be populated for all products
6. Offer Type must match approved offer type classifications
7. Business Entity should align with organizational structure

---

## Attribute Details

### product_key
- **Data Type**: integer
- **Nullable**: No
- **Primary Key**: Yes
- **Description**: Surrogate key that uniquely identifies a product record in the product dimension

### product_id
- **Data Type**: character varying(30)
- **Nullable**: No
- **Description**: Business identifier or SKU assigned to the product or subscription offer

### product_name
- **Data Type**: character varying(80)
- **Nullable**: Yes
- **Description**: Descriptive name of the product, service, or subscription offer

### product_family
- **Data Type**: character varying(30)
- **Nullable**: Yes
- **Description**: Higher-level grouping of related products within the portfolio

### technology_domain
- **Data Type**: character varying(40)
- **Nullable**: Yes
- **Description**: Technology area to which the product belongs, such as networking, security, or collaboration

### offer_type
- **Data Type**: character varying(30)
- **Nullable**: Yes
- **Description**: Commercial offer classification, such as hardware, SaaS subscription, or software subscription

### business_entity
- **Data Type**: character varying(30)
- **Nullable**: Yes
- **Description**: Internal business portfolio or organizational entity responsible for the product

---

## Analytical Use Cases

- Analyze sales performance by product and product family
- Track revenue by technology domain
- Evaluate offer type mix and trends
- Monitor business entity contribution
- Identify product adoption patterns
- Support product strategy and planning

---

## Data Quality Metrics

- **Completeness**: Product Key and Product ID must be 100% populated
- **Uniqueness**: Product Key and Product ID must be unique
- **Validity**: Product Family, Technology Domain, and Offer Type must match approved values
- **Consistency**: Product attributes must align with product catalog

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Bundle Index](../index.md)
