---
title: Product to Booking Transaction
type: relationship
description: Foreign key relationship linking products and offers to booking transactions
resource: relationships
tags: [relationship, foreign-key, product, booking, one-to-many, portfolio]
timestamp: 2026-07-28T00:00:00Z
---

# Product to Booking Transaction

## Business Definition

Links products and offers to booking transactions, enabling analysis of product portfolio performance by product family, technology domain, offer type, and business entity to support product strategy and portfolio optimization.

---

## Relationship Details

**Relationship ID**: REL006  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Product](../entities/product.md)  
**Attribute**: Product Key (product_key)  
**Role**: Parent/Dimension

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Product Key (product_key)  
**Role**: Child/Fact

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_product  
**Source Column**: product_key  
**Target Table**: QuoteToBooking.fact_bookings  
**Target Column**: product_key  
**Join Type**: INNER JOIN

---

## Business Description

Each booking transaction is associated with exactly one product or offer that was sold to the customer. A single product can have multiple booking transactions as it is sold to multiple customers over time.

This relationship enables business users to:
- Analyze booking amounts by product family
- Compare technology domain performance
- Evaluate offer type effectiveness
- Identify top-selling products
- Assess business entity portfolio performance
- Track product adoption and market penetration

---

## Relationship Rules

1. **Cardinality**: One product can have many booking transactions (One-to-Many)
2. **Referential Integrity**: Every booking transaction must reference a valid product record
3. **Mandatory**: Product Key is required in booking transactions for product analysis
4. **Immutable**: Product association should not change after booking is recorded

---

## Usage Examples

### Analyze Bookings by Product Family
```sql
SELECT p.product_family, SUM(b.booking_amount_usd)
FROM dim_product p
JOIN fact_bookings b ON p.product_key = b.product_key
GROUP BY p.product_family
```

### Compare Technology Domain Performance
```sql
SELECT p.technology_domain, SUM(b.booking_amount_usd), SUM(b.quantity)
FROM dim_product p
JOIN fact_bookings b ON p.product_key = b.product_key
GROUP BY p.technology_domain
ORDER BY SUM(b.booking_amount_usd) DESC
```

---

## Related Concepts

### Related Entities
- [Product](../entities/product.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)

### Related Glossary Terms
- [Product](../glossary/product.md)
- [Product Key](../glossary/product-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [View Relationships Index](index.md)
- [View Product Entity](../entities/product.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Relationship ID**: REL006  
**Source**: Product  
**Target**: Booking Transaction  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Last Updated**: 2026-07-28T00:00:00Z
