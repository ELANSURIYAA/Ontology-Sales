---
title: Product
type: entity
description: Products and offers sold to customers including product family, technology domain, offer type, and business entity
resource: entities
tags: [product, offer, catalog, dimension, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Product

## Business Definition

The Product entity stores descriptive information about products and offers sold to customers. It captures product characteristics including product family, technology domain, offer type, and business entity. This entity enables product portfolio analysis, technology domain performance tracking, and offer type segmentation.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_product  
**Source Schema**: QuoteToBooking  
**Entity Type**: Dimension  
**Entity ID**: ENT006

---

## Attributes

- **Product Key** - Surrogate key that uniquely identifies a product record in the product dimension
- **Product ID** - Business identifier or SKU assigned to the product or offer
- **Product Name** - Commercial name of the product or subscription offer sold to the customer
- **Product Family** - Higher-level product grouping used for portfolio and performance analysis
- **Technology Domain** - Technology area or solution domain to which the product belongs
- **Offer Type** - Indicates whether the item is sold as hardware, software subscription, or SaaS subscription
- **Business Entity** - Internal business unit or portfolio responsible for the product

---

## Primary Keys

- **Product Key** (product_key) - Surrogate key, Integer, Not Nullable

---

## Foreign Keys

None - This is a dimension entity

---

## Relationships

### Outgoing Relationships

- **[Product to Booking Transaction](../relationships/product-to-booking-transaction.md)** - One-to-Many relationship linking products to booking transactions

### Related Entities

- **[Booking Transaction](./booking-transaction.md)** - Fact entity containing booking records for products
- **[Customer](./customer.md)** - Customers purchasing products
- **[Contract](./contract.md)** - Contracts covering product subscriptions
- **[Partner](./partner.md)** - Partners selling products

---

## Measures

Products support portfolio analysis of all measures:

- **[Booking Amount USD](../measures/booking-amount-usd.md)** - Revenue by product and family
- **[Annual Contract Value USD](../measures/annual-contract-value-usd.md)** - ACV by technology domain
- **[Total Contract Value USD](../measures/total-contract-value-usd.md)** - TCV by offer type
- **[Quantity Sold](../measures/quantity-sold.md)** - Volume by product
- **[Discount Percentage](../measures/discount-percentage.md)** - Product pricing patterns
- **[Unit List Price USD](../measures/unit-list-price-usd.md)** - Product pricing strategy

---

## Business Rules

1. Product Key must be unique and not null
2. Product ID must be unique and not null
3. Product Name is required for all product records
4. Product Family must be from approved product catalog
5. Technology Domain must be from approved domain list (Networking, Security, Collaboration, Observability, etc.)
6. Offer Type must be from approved list (Hardware, Software Subscription, SaaS Subscription)
7. Business Entity must be from approved organizational structure
8. Each product must belong to exactly one product family
9. Each product must map to exactly one technology domain

---

## Analytical Usage

### Product Family Analysis
- Compare booking performance across product families
- Track product family mix and trends
- Analyze portfolio contribution by family

### Technology Domain Analysis
- Evaluate performance by technology area (Networking, Security, Collaboration, etc.)
- Track technology domain adoption and growth
- Analyze solution domain revenue contribution

### Offer Type Analysis
- Compare hardware vs software vs SaaS booking patterns
- Track subscription vs perpetual license mix
- Analyze offer type trends and transitions

### Business Entity Analysis
- Evaluate performance by internal business unit
- Track portfolio responsibility and ownership
- Analyze cross-portfolio opportunities

---

## Product Hierarchy

```
Business Entity
  └─ Technology Domain
      └─ Product Family
          └─ Product Name
```

### Example Hierarchy

```
Enterprise Networking
  ├─ Networking
  │   ├─ Switching Family
  │   │   ├─ Campus Switch Pro
  │   │   └─ Data Center Switch Elite
  │   └─ Routing Family
  │       ├─ Edge Router Standard
  │       └─ Core Router Advanced
  └─ Security
      ├─ Firewall Family
      │   ├─ Next-Gen Firewall
      │   └─ Cloud Firewall
      └─ Threat Detection Family
          └─ Advanced Threat Protection

Collaboration
  └─ Collaboration
      ├─ Unified Communications
      │   ├─ Video Conferencing Pro
      │   └─ Team Collaboration Suite
      └─ Contact Center
          └─ Cloud Contact Center

Software & Services
  ├─ Observability
  │   └─ Monitoring Family
  │       ├─ Network Monitoring Platform
  │       └─ Application Performance Monitor
  └─ Software Subscription
      └─ Enterprise Software Suite
```

---

## Related Concepts

- **[Customer](./customer.md)** - Customers purchasing products
- **[Contract](./contract.md)** - Product subscription agreements
- **[Partner](./partner.md)** - Channel partners selling products
- **[Sales Representative](./sales-representative.md)** - Sales personnel selling products
- **[Booking Transaction](./booking-transaction.md)** - Product sales transactions

---

## Glossary Terms

- [Product](../glossary/product.md)
- [Product Key](../glossary/product-key.md)
- [Product ID](../glossary/product-id.md)
- [Product Name](../glossary/product-name.md)
- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Offer Type](../glossary/offer-type.md)
- [Business Entity](../glossary/business-entity.md)

---

## Attribute Details

| Attribute | Technical Column | Data Type | Nullable | Key Type | Description |
|-----------|-----------------|-----------|----------|----------|-------------|
| Product Key | product_key | integer | No | Primary | Surrogate key uniquely identifying product |
| Product ID | product_id | character varying(30) | No | Business | Business identifier or SKU for product |
| Product Name | product_name | character varying(80) | Yes | - | Commercial name of product or offer |
| Product Family | product_family | character varying(30) | Yes | - | Higher-level product grouping |
| Technology Domain | technology_domain | character varying(40) | Yes | - | Technology area or solution domain |
| Offer Type | offer_type | character varying(30) | Yes | - | Product delivery model classification |
| Business Entity | business_entity | character varying(30) | Yes | - | Internal business unit ownership |

---

## Semantic Links

- [Entity Index](./index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Relationship Index](../relationships/index.md)
- [Measure Index](../measures/index.md)
- [Main Index](../index.md)

---

## Metadata

**Entity ID**: ENT006  
**Domain ID**: DOM001  
**Entity Type**: Dimension  
**Technical Table**: QuoteToBooking.dim_product  
**Total Attributes**: 7  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
