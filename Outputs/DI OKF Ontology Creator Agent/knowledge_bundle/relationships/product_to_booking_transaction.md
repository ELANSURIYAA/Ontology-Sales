---
title: Product to Booking Transaction
type: relationship
description: One-to-many foreign key relationship from Product to Booking Transaction.
resource: relationships
tags: relationship,product,booking transaction,foreign key
timestamp: 2026-07-28T00:00:00Z
---

# Product to Booking Transaction

## Source Entity

- [Product](../entities/product.md)

---

## Target Entity

- [Booking Transaction](../entities/booking_transaction.md)

---

## Relationship Type

Foreign Key

---

## Cardinality

One-to-Many

---

## Business Description

A product can be associated with multiple booking transactions. The booking transaction stores Product Key as a foreign key to provide portfolio and offer context for each completed booking.

---

## Technical Mapping

- Parent Attribute: Product Key
- Child Attribute: Product Key
- Confidence Score: 1.00

---

## Semantic Cross Links

- [Relationships Index](index.md)
- [Product](../entities/product.md)
- [Booking Transaction](../entities/booking_transaction.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Glossary: Product Key](../glossary/product_key.md)
