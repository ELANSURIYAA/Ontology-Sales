---
title: Booking ID
type: glossary
description: Unique identifier for an individual booking transaction record
resource: glossary
tags: [booking-id, identifier, primary-key]
timestamp: 2024-01-15T00:00:00Z
---

# Booking ID

## Business Definition

Unique identifier for an individual booking transaction record. This identifier serves as the primary key for the booking transaction entity.

---

## Business Meaning

Booking ID uniquely identifies each booking transaction in the system. It is used to track individual sales bookings and serves as the grain for all booking-level analysis.

---

## Technical Mapping

**Source Field**: bookings.booking_id  
**Data Type**: Identifier  
**Key Type**: Primary Key

---

## Synonyms

- Booking Transaction ID
- Transaction ID
- Booking Record ID

---

## Related Concepts

- [Order Number](order-number.md)
- [Order Line Number](order-line-number.md)
- [Booking Transaction](../entities/bookings.md)

---

## Usage Context

Booking ID is used in:
- Uniquely identifying booking transactions
- Counting distinct bookings
- Joining booking data with dimensional attributes
- Transaction-level analysis and reporting

---

## Navigation

- [Return to Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Bookings Domain](../domains/bookings.md)
