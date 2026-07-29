---
title: Order Number
type: glossary
description: Business order number associated with the booking transaction
resource: glossary
tags: [booking, transaction, order, identifier, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Order Number

## Business Definition

Business order number associated with the booking transaction.

---

## Business Meaning

Order Number is the business-recognized identifier for the customer order that generated the booking transaction. It provides traceability to source order systems and enables order-level analysis.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Source Column:** order_number  
**Data Type:** Character Varying(20)  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Attribute:** Order Number  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Parent entity
- [Booking ID](./booking-id.md) - Transaction identifier
- [Order Line Number](./order-line-number.md) - Line item reference

---

## Usage Context

Order Number is used to:
- Reference source customer orders
- Enable order-level aggregation
- Support order tracking and traceability
- Link to operational order systems

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
