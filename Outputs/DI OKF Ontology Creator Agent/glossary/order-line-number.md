---
title: Order Line Number
type: glossary
description: Line number within the sales order that identifies the specific booked item
resource: glossary
tags: [okf, glossary, attribute, booking, order]
timestamp: 2026-07-28T00:00:00Z
---

# Order Line Number

## Business Definition

Line number within the sales order that identifies the specific booked item.

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings  
**Source Column**: order_line_number  
**Entity**: Booking Fact  
**Attribute**: Order Line Number

---

## Business Meaning

Order Line Number identifies the specific line item within a sales order. Combined with the Order Number, it provides a unique business key for identifying individual booking transactions.

---

## Synonyms

- Line Number
- Line Item Number

---

## Related Concepts

- [Booking Fact](booking-fact.md)
- [Order Number](order-number.md)
- [Booking ID](booking-id.md)

---

## Navigation

- [Back to Glossary Index](index.md)
- [Back to Bundle Index](../index.md)
