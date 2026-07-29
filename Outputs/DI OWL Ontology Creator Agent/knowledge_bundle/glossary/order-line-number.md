---
title: Order Line Number
type: glossary
description: Line item number within the order associated with the booking
resource: glossary
tags: [booking, transaction, order, line, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Order Line Number

## Business Definition

Line item number within the order associated with the booking.

---

## Business Meaning

Order Line Number identifies the specific line item within a customer order that corresponds to the booking transaction. Combined with Order Number, it provides unique identification of the source order line.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Source Column:** order_line_number  
**Data Type:** Integer  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Attribute:** Order Line Number  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Parent entity
- [Order Number](./order-number.md) - Order reference
- [Booking ID](./booking-id.md) - Transaction identifier

---

## Usage Context

Order Line Number is used to:
- Identify specific line items within orders
- Enable line-level traceability
- Support detailed order analysis
- Link to source order line items

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
