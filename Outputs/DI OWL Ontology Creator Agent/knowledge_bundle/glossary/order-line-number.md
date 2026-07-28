---
title: Order Line Number
type: glossary
description: Line item number within the order associated with the booking
resource: glossary
tags: [glossary, booking, order, line-item]
timestamp: 2026-07-28T00:00:00Z
---

# Order Line Number

## Business Definition

Line item number within the order associated with the booking.

---

## Business Meaning

Order Line Number identifies the specific line item within a customer order. When combined with Order Number, it uniquely identifies a specific product or service within an order. Orders typically contain multiple line items, each representing a different product, quantity, or configuration.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Source Column**: order_line_number

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Attribute**: Order Line Number

**Data Type**: Integer

**Confidence Score**: 1.00

---

## Related Concepts

- [Booking Transaction](booking-transaction.md)
- [Booking ID](booking-id.md)
- [Order Number](order-number.md)

---

## Usage Context

Order Line Number is used to:
- Identify specific line items within orders
- Support order detail tracking
- Enable line-item level analysis
- Facilitate fulfillment operations
- Support order reconciliation

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
