---
title: Customer to Booking Transaction
type: relationship
description: One-to-many foreign key relationship from Customer to Booking Transaction.
resource: relationships
tags: relationship,customer,booking transaction,foreign key
timestamp: 2026-07-28T00:00:00Z
---

# Customer to Booking Transaction

## Source Entity

- [Customer](../entities/customer.md)

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

A customer can be associated with multiple booking transactions. The booking transaction stores Customer Key as a foreign key to provide customer context for each completed booking.

---

## Technical Mapping

- Parent Attribute: Customer Key
- Child Attribute: Customer Key
- Confidence Score: 1.00

---

## Semantic Cross Links

- [Relationships Index](index.md)
- [Customer](../entities/customer.md)
- [Booking Transaction](../entities/booking_transaction.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Glossary: Customer Key](../glossary/customer_key.md)
