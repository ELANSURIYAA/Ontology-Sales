---
title: Order Number
type: glossary
description: Sales order number associated with the booking transaction
resource: glossary
tags: [okf, glossary, attribute, booking, order]
timestamp: 2026-07-28T00:00:00Z
---

# Order Number

## Business Definition

Sales order number associated with the booking transaction.

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings  
**Source Column**: order_number  
**Entity**: Booking Fact  
**Attribute**: Order Number

---

## Business Meaning

Order Number is the business identifier for the sales order that contains the booking transaction. Multiple booking lines may share the same order number, with each line distinguished by the order line number.

---

## Synonyms

- Sales Order Number
- Order ID

---

## Related Concepts

- [Booking Fact](booking-fact.md)
- [Booking ID](booking-id.md)
- [Order Line Number](order-line-number.md)

---

## Navigation

- [Back to Glossary Index](index.md)
- [Back to Bundle Index](../index.md)
