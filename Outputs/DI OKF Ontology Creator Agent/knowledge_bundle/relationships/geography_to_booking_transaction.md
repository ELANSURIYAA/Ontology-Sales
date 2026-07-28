---
title: Geography to Booking Transaction
type: relationship
description: One-to-many foreign key relationship from Geography to Booking Transaction.
resource: relationships
tags: relationship,geography,booking transaction,foreign key
timestamp: 2026-07-28T00:00:00Z
---

# Geography to Booking Transaction

## Source Entity

- [Geography](../entities/geography.md)

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

A geography can be associated with multiple booking transactions. The booking transaction stores Geography Key as a foreign key to provide regional reporting context for each completed booking.

---

## Technical Mapping

- Parent Attribute: Geography Key
- Child Attribute: Geography Key
- Confidence Score: 1.00

---

## Semantic Cross Links

- [Relationships Index](index.md)
- [Geography](../entities/geography.md)
- [Booking Transaction](../entities/booking_transaction.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Glossary: Geography Key](../glossary/geography_key.md)
