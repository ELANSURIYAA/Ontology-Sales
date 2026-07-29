---
title: Booking ID
type: glossary
description: Unique identifier for an individual booking transaction record
resource: glossary
tags: [booking, transaction, identifier, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Booking ID

## Business Definition

Unique identifier for an individual booking transaction record.

---

## Business Meaning

Booking ID is the primary key that uniquely identifies each booking transaction in the fact table. It serves as the definitive identifier for individual sales events.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Source Column:** booking_id  
**Data Type:** Integer  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Attribute:** Booking ID  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Parent entity
- [Order Number](./order-number.md) - Business order reference
- [Order Line Number](./order-line-number.md) - Line item reference

---

## Usage Context

Booking ID is used to:
- Uniquely identify each booking transaction
- Support transaction-level analysis
- Enable drill-down to individual bookings
- Provide referential integrity for fact records

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
