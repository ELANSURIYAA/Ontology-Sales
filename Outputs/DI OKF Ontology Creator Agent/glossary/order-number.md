---
title: Order Number
type: glossary
description: Sales order number associated with the booking transaction
resource: glossary
tags: [order-number, identifier, order]
timestamp: 2024-01-15T00:00:00Z
---

# Order Number

## Business Definition

Sales order number associated with the booking transaction. This identifier represents the sales order that contains one or more booking line items.

---

## Business Meaning

Order Number identifies the sales order document that contains the booking transaction. A single order can have multiple line items (booking transactions), each with a unique order line number. Order Number is used to group related booking transactions and analyze order-level metrics.

---

## Technical Mapping

**Source Field**: bookings.order_number  
**Data Type**: Identifier  
**Key Type**: Business Key

---

## Synonyms

- Sales Order Number
- Order ID
- SO Number

---

## Related Concepts

- [Order Line Number](order-line-number.md)
- [Booking ID](booking-id.md)
- [Booking Transaction](../entities/bookings.md)

---

## Usage Context

Order Number is used in:
- Grouping booking transactions by order
- Counting distinct orders
- Order-level analysis and reporting
- Tracking multi-line orders

---

## Navigation

- [Return to Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Distinct Order Count Measure](../measures/distinct-order-count.md)
