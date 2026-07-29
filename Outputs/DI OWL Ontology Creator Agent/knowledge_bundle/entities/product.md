---
title: Product
type: entity
description: Products and offers sold to customers including product family, technology domain, offer type, and business entity
resource: entities
tags: [product, offer, sku, portfolio, dimension]
timestamp: 2026-07-28T00:00:00Z
---

# Product

## Business Definition

Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity. Products represent the goods and services that generate revenue through customer bookings.

---

## Entity Identifier

**Entity ID:** ENT006  
**Domain:** [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_product  
**Table Type:** Dimension Table

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

- **Product Key** (product_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- **[Product to Booking Transaction](../relationships/product-to-booking-transaction.md)** - One-to-Many relationship linking products to booking transactions

---

## Measures

Products are analyzed using measures from related [Booking Transaction](./booking-transaction.md) entity:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Business Rules

1. Each product must have a unique Product Key
2. Product ID serves as the business SKU identifier
3. Product Family enables portfolio-level analysis
4. Technology Domain categorizes products by solution area
5. Offer Type distinguishes hardware, software, and SaaS offerings
6. Business Entity identifies the responsible organizational unit

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Transactions involving this product
- [Customer](./customer.md) - Customers purchasing products
- [Partner](./partner.md) - Partners selling products
- [Contract](./contract.md) - Contracts covering products
- [Geography](./geography.md) - Geographic markets for products

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

## Navigation

- [Return to Entities Index](./index.md)
- [Return to Bundle Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
- [View Relationships](../relationships/index.md)
