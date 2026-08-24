---
title: Products
type: entity
description: Stores descriptive information about products and offers sold to customers, including product identity, family, technology domain, offer type, and business entity
resource: entities
tags: [products, dimension, product-family, technology-domain]
timestamp: 2026-07-28T00:00:00Z
---

# Products

## Business Definition

The Products entity represents the dimension table that stores descriptive information about products and service offers sold to customers. Each record contains product identity attributes, product family groupings, technology domain classifications, offer type categorizations, and business entity associations. This entity enables analysis of booking transactions by product characteristics and supports product portfolio management.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_product

**Source Schema**: quotetobooking

**Entity Type**: Dimension Table

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

All booking-related measures can be analyzed by product attributes:
- [Booking Count](../measures/booking-count.md)
- [Total Quantity](../measures/total-quantity.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Average Discount Percentage](../measures/average-discount-pct.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)

---

## Related Concepts

- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

1. **Unique Product Key**: Each product record must have a unique product_key
2. **Product Identifier**: product_id represents the business identifier or SKU for the product
3. **Product Family Grouping**: Products are grouped into families representing related offerings
4. **Technology Domain Classification**: Products are classified by technology area or solution domain
5. **Offer Type Categorization**: Products are categorized by commercial offer type (hardware, software subscription, SaaS subscription)
6. **Business Entity Association**: Products are associated with internal business portfolios or organizational units

---

## Attribute Definitions

### product_key
Surrogate key that uniquely identifies a product record in the product dimension. Used as the primary key and referenced by the bookings fact table.

### product_id
Business identifier or SKU assigned to the product or offer. Represents the natural key used in operational systems.

### product_name
Descriptive name of the product or service offering. Used for reporting and product identification.

### product_family
Higher-level grouping of related products within the portfolio. Enables product family analysis and portfolio management.

### technology_domain
Technology area or solution domain the product belongs to. Used for technology-specific analysis and strategic planning.

### offer_type
Commercial offer classification, such as hardware, software subscription, or SaaS subscription. Enables offer type analysis and revenue model tracking.

### business_entity
Internal business portfolio or organizational unit associated with the product. Used for business unit reporting and accountability.

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Usage Examples

### Product Family Analysis
- Analyze booking amount by product family
- Track product family performance trends
- Identify top-performing product families

### Technology Domain Analysis
- Evaluate technology domain adoption rates
- Compare booking performance across domains
- Identify strategic technology investments

### Offer Type Analysis
- Analyze revenue mix by offer type
- Track subscription vs hardware revenue
- Monitor SaaS adoption trends

### Business Entity Analysis
- Track booking performance by business unit
- Allocate revenue to organizational units
- Support business unit accountability

---

## Data Quality Checks

- product_key is unique and not null
- product_id is not null
- product_name is not null
- product_family is a valid family designation
- technology_domain is a valid domain classification
- offer_type is a valid offer type
- business_entity is a valid business unit
