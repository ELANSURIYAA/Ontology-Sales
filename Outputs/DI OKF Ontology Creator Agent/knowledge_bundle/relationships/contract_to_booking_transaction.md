---
title: Contract to Booking Transaction
type: relationship
description: One-to-many foreign key relationship from Contract to Booking Transaction.
resource: relationships
tags: relationship,contract,booking transaction,foreign key
timestamp: 2026-07-28T00:00:00Z
---

# Contract to Booking Transaction

## Source Entity

- [Contract](../entities/contract.md)

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

A contract can be associated with multiple booking transactions. The booking transaction stores Contract Key as a foreign key to provide the commercial agreement context for each booking.

---

## Technical Mapping

- Parent Attribute: Contract Key
- Child Attribute: Contract Key
- Confidence Score: 1.00

---

## Semantic Cross Links

- [Relationships Index](index.md)
- [Contract](../entities/contract.md)
- [Booking Transaction](../entities/booking_transaction.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Glossary: Contract Key](../glossary/contract_key.md)
