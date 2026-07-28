---
title: Product to Booking Transaction
type: relationship
description: One-to-Many relationship linking products to booking transactions
resource: relationships
tags: [relationship, foreign-key, product, booking-transaction, portfolio]
timestamp: 2026-07-28T00:00:00Z
---

# Product to Booking Transaction

## Business Description

This relationship links product records to booking transactions, enabling analysis of bookings by product family, technology domain, offer type, and business entity.

---

## Relationship Details

**Source Entity**: [Product](../entities/product.md)

**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Relationship Type**: Foreign Key

**Cardinality**: One-to-Many

**Confidence Score**: 1.00

---

## Technical Mapping

**Parent Table**: QuoteToBooking.dim_product

**Parent Column**: product_key

**Child Table**: QuoteToBooking.fact_bookings

**Child Column**: product_key

---

## Cardinality Explanation

- **One Product** can be associated with **Many Booking Transactions**
- **Each Booking Transaction** must reference **exactly one Product**

This relationship enables:
- Analysis of booking amounts by product family
- Evaluation of technology domain performance
- Measurement of offer type adoption
- Product portfolio analysis

---

## Business Rules

1. Every booking transaction must reference a valid product
2. A product can be associated with zero or many booking transactions
3. Product Key is the foreign key in the booking transaction fact table
4. The relationship is mandatory on the booking transaction side
5. The relationship supports referential integrity

---

## Related Concepts

- [Product](../glossary/product.md)
- [Product Key](../glossary/product-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Offer Type](../glossary/offer-type.md)

---

## Usage Examples

**Analyze bookings by product family**:
- Compare product family performance
- Measure product family contribution to revenue

**Analyze bookings by technology domain**:
- Evaluate networking vs. security vs. collaboration performance
- Measure technology domain adoption

**Analyze bookings by offer type**:
- Compare hardware vs. software subscription vs. SaaS subscription
- Measure subscription adoption trends

**Product performance analysis**:
- Identify top-performing products
- Analyze product mix by customer segment
- Measure product adoption by geography

---

## Navigation

- [Back to Relationships Index](index.md)
- [View Source Entity: Product](../entities/product.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
