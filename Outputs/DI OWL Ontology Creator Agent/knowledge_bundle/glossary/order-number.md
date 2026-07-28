---
title: Order Number
type: glossary
description: Business order number associated with the booking transaction
resource: glossary
tags: [glossary, booking, order, identifier]
timestamp: 2026-07-28T00:00:00Z
---

# Order Number

## Business Definition

Business order number associated with the booking transaction.

---

## Business Meaning

Order Number is the business-recognized identifier for the customer order that generated the booking transaction. Multiple booking transactions (line items) can share the same order number. Order numbers are used in operational systems, customer communications, and fulfillment processes to track and manage customer orders.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Source Column**: order_number

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Attribute**: Order Number

**Data Type**: Character Varying(20)

**Confidence Score**: 1.00

---

## Related Concepts

- [Booking Transaction](booking-transaction.md)
- [Booking ID](booking-id.md)
- [Order Line Number](order-line-number.md)

---

## Usage Context

Order Number is used to:
- Identify customer orders
- Group related booking transactions
- Support order tracking and fulfillment
- Enable order-level analysis
- Facilitate customer service operations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
