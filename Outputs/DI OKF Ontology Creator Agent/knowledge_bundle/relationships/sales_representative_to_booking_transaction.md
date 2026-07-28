---
title: Sales Representative to Booking Transaction
type: relationship
description: One-to-many foreign key relationship from Sales Representative to Booking Transaction.
resource: relationships
tags: relationship,sales representative,booking transaction,foreign key
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative to Booking Transaction

## Source Entity

- [Sales Representative](../entities/sales_representative.md)

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

A sales representative can be associated with multiple booking transactions. The booking transaction stores Sales Representative Key as a foreign key to provide sales ownership and coverage context for each completed booking.

---

## Technical Mapping

- Parent Attribute: Sales Representative Key
- Child Attribute: Sales Representative Key
- Confidence Score: 1.00

---

## Semantic Cross Links

- [Relationships Index](index.md)
- [Sales Representative](../entities/sales_representative.md)
- [Booking Transaction](../entities/booking_transaction.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Glossary: Sales Representative Key](../glossary/sales_representative_key.md)
