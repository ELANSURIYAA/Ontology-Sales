---
title: Product Management Domain
type: domain
description: Product and offer master data used to analyze bookings by product identity, family, and technology domain
resource: domains
tags: [okf, domain, product-management, product, portfolio]
timestamp: 2026-07-28T00:00:00Z
---

# Product Management Domain

## Business Definition

The Product Management domain encompasses product and offer master data used to analyze bookings by product identity, family, technology domain, offer type, and business entity. This domain provides the product dimensional context necessary for product portfolio analytics.

---

## Business Purpose

This domain enables business users to:

- Analyze sales performance by product and product family
- Track revenue by technology domain
- Evaluate offer type mix and trends
- Monitor business entity contribution
- Identify product adoption patterns
- Measure product portfolio performance
- Support product strategy and planning

---

## Domain Scope

### Included
- Product identity and identification
- Product family hierarchies
- Technology domain classifications
- Offer type categorizations
- Business entity assignments
- Product descriptive attributes

### Excluded
- Product pricing details (covered in Pricing domain)
- Product inventory and availability
- Product technical specifications
- Product lifecycle management
- Product development roadmaps

---

## Related Entities

### Primary Entities
- [Product Dimension](../entities/product-dimension.md)

---

## Related Measures

All sales and revenue measures can be analyzed by product attributes:

- [Quantity Sold](../measures/quantity-sold.md) by product
- [Booking Amount USD](../measures/booking-amount-usd.md) by product
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md) by product
- [Total Contract Value USD](../measures/total-contract-value-usd.md) by product
- [Unit List Price USD](../measures/unit-list-price-usd.md) by product
- [Discount Percentage](../measures/discount-percentage.md) by product

---

## Related Relationships

- [Product to Booking](../relationships/product-to-booking.md)

---

## Key Business Concepts

### Product Identity
Each product or offer is uniquely identified by a Product ID (SKU) and has a descriptive Product Name for business reporting.

### Product Family
Higher-level grouping of related products within the portfolio, enabling family-level analysis and reporting.

### Technology Domain
Technology area classification such as:
- Networking
- Security
- Collaboration
- Data Center
- Cloud Services

### Offer Type
Commercial offer classification such as:
- Hardware
- Software Subscription
- SaaS Subscription
- Professional Services
- Support and Maintenance

### Business Entity
Internal business portfolio or organizational entity responsible for the product, enabling P&L and business unit analysis.

---

## Business Rules

1. Every product must have a unique Product Key (surrogate key)
2. Every product must have a unique Product ID (business key/SKU)
3. Product Name is required for reporting and analysis
4. Product Family should be populated for all products
5. Technology Domain should be populated for all products
6. Offer Type must match approved offer type classifications
7. Business Entity should align with organizational structure

---

## Analytical Use Cases

### Product Performance Analysis
- Track revenue and bookings by product
- Identify top performing products
- Analyze product growth trends
- Monitor product lifecycle stages

### Product Family Analysis
- Compare performance across product families
- Analyze family contribution to total revenue
- Identify cross-sell and upsell opportunities within families
- Track family-level market share

### Technology Domain Analysis
- Analyze revenue by technology domain
- Identify domain-specific trends and opportunities
- Compare domain performance and growth rates
- Support technology investment decisions

### Offer Type Analysis
- Analyze mix of hardware, software, and services
- Track subscription versus perpetual license trends
- Monitor recurring revenue by offer type
- Evaluate offer type profitability

### Business Entity Analysis
- Track revenue by business entity for P&L reporting
- Compare business entity performance
- Analyze portfolio contribution
- Support organizational planning

---

## Data Quality Metrics

### Completeness
- Product Key must be populated for all records
- Product ID must be populated for all records
- Product Name must be populated for all records
- Product Family should be populated (>95% target)
- Technology Domain should be populated (>95% target)

### Accuracy
- Product ID must be unique
- Product Family must match approved family values
- Technology Domain must match approved domain values
- Offer Type must match approved offer type values
- Business Entity must match organizational structure

### Consistency
- Product attributes must be consistent across all bookings
- Product master data must reconcile with source product catalog
- Product hierarchies must be logically consistent

---

## Technical Implementation

### Source System
- **Schema**: quotetobooking
- **Table**: dim_product
- **Primary Key**: product_key (surrogate key)
- **Business Key**: product_id
- **Type**: Slowly Changing Dimension (Type 1 or Type 2)

### Key Attributes
- Product Key (Primary Key)
- Product ID (Business Key/SKU)
- Product Name
- Product Family
- Technology Domain
- Offer Type
- Business Entity

---

## Semantic Links

### Related Domains
- [Sales Transactions](sales-transactions.md)
- [Pricing](pricing.md)
- [Revenue Metrics](revenue-metrics.md)
- [Contract Management](contract-management.md)

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

## Navigation

- [Back to Domains Index](index.md)
- [Back to Bundle Index](../index.md)
