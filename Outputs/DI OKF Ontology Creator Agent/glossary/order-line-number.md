---
title: Order Line Number
type: glossary
description: Line number within the sales order representing the booked item or service
resource: glossary
tags: [order-line, line-number, order]
timestamp: 2024-01-15T00:00:00Z
---

# Order Line Number

## Business Definition

Line number within the sales order representing the booked item or service. This identifier distinguishes individual line items within a multi-line order.

---

## Business Meaning

Order Line Number identifies the specific line item within a sales order. Combined with Order Number, it provides a unique business key for each booking transaction. Line numbers enable tracking of individual products or services within a single order.

---

## Technical Mapping

**Source Field**: bookings.order_line_number  
**Data Type**: Identifier  
**Key Type**: Business Key Component

---

## Synonyms

- Line Item Number
- Order Line
- Line Number

---

## Related Concepts

- [Order Number](order-number.md)
- [Booking ID](booking-id.md)
- [Booking Transaction](../entities/bookings.md)

---

## Usage Context

Order Line Number is used in:
- Identifying specific line items within an order
- Distinguishing multiple products in a single order
- Line-level analysis and reporting
- Order composition analysis

---

## Navigation

- [Return to Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Bookings Domain](../domains/bookings.md)
