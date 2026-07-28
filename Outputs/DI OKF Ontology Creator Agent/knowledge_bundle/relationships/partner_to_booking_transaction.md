---
title: Partner to Booking Transaction
type: relationship
description: One-to-many foreign key relationship from Partner to Booking Transaction.
resource: relationships
tags: relationship,partner,booking transaction,foreign key
timestamp: 2026-07-28T00:00:00Z
---

# Partner to Booking Transaction

## Source Entity

- [Partner](../entities/partner.md)

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

A partner can be associated with multiple booking transactions. The booking transaction stores Partner Key as a foreign key to provide route-to-market and partner participation context for each completed booking.

---

## Technical Mapping

- Parent Attribute: Partner Key
- Child Attribute: Partner Key
- Confidence Score: 1.00

---

## Semantic Cross Links

- [Relationships Index](index.md)
- [Partner](../entities/partner.md)
- [Booking Transaction](../entities/booking_transaction.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Glossary: Partner Key](../glossary/partner_key.md)
