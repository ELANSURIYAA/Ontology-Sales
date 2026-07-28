---
title: Date to Booking Transaction
type: relationship
description: One-to-many foreign key relationship from Date to Booking Transaction.
resource: relationships
tags: relationship,date,booking transaction,foreign key
timestamp: 2026-07-28T00:00:00Z
---

# Date to Booking Transaction

## Source Entity

- [Date](../entities/date.md)

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

A date can be associated with multiple booking transactions. The booking transaction stores Booking Date Key as a foreign key to provide reporting period context for each completed booking.

---

## Technical Mapping

- Parent Attribute: Date Key
- Child Attribute: Booking Date Key
- Confidence Score: 1.00

---

## Semantic Cross Links

- [Relationships Index](index.md)
- [Date](../entities/date.md)
- [Booking Transaction](../entities/booking_transaction.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Glossary: Date Key](../glossary/date_key.md)
