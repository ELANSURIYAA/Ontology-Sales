---
title: Product to Booking Transaction
type: relationship
description: Foreign key relationship linking products to booking transactions
resource: relationships
tags: [product, booking, foreign-key, one-to-many, portfolio]
timestamp: 2026-07-28T00:00:00Z
---

# Product to Booking Transaction

## Relationship Definition

Links product records to booking transactions, enabling analysis of bookings by product family, technology domain, offer type, and business entity. This relationship allows business users to understand product portfolio performance and revenue contribution.

---

## Relationship Identifier

**Relationship ID:** REL006

---

## Source Entity

**[Product](../entities/product.md)**  
**Entity ID:** ENT006  
**Technical Table:** QuoteToBooking.dim_product

---

## Target Entity

**[Booking Transaction](../entities/booking-transaction.md)**  
**Entity ID:** ENT008  
**Technical Table:** QuoteToBooking.fact_bookings

---

## Relationship Type

**Type:** Foreign Key  
**Cardinality:** One-to-Many  
**Confidence Score:** 1.00

---

## Technical Mapping

**Parent Attribute:** Product Key (product_key)  
**Child Attribute:** Product Key (product_key)  
**Join Condition:** dim_product.product_key = fact_bookings.product_key

---

## Business Description

Each product can be associated with multiple booking transactions, but each booking transaction involves exactly one product. This relationship enables analysis of:

- Booking performance by product family
- Revenue contribution by technology domain
- Offer type mix analysis (hardware, software, SaaS)
- Business entity portfolio performance
- Product-level profitability

---

## Related Measures

This relationship enables product-based analysis of:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Business Use Cases

1. **Product Family Analysis** - Compare booking performance across product families
2. **Technology Domain Analysis** - Evaluate revenue contribution by solution domain
3. **Offer Type Analysis** - Analyze booking mix between hardware, software, and SaaS
4. **Portfolio Performance** - Track business entity portfolio revenue and growth
5. **Product Pricing** - Analyze pricing and discount patterns by product

---

## Navigation

- [Return to Relationships Index](./index.md)
- [View Source Entity: Product](../entities/product.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
