---
title: Order Line Number
type: glossary
description: Line item number within the order associated with the booking
resource: glossary
tags: [glossary, booking, order-line, line-item]
timestamp: 2026-07-28T00:00:00Z
---

# Order Line Number

## Business Definition

Line item number within the order associated with the booking.

---

## Business Meaning

Order Line Number identifies the specific line item within a multi-line order. Orders may contain multiple products or services, and each line represents a distinct item. The order line number enables tracking of individual items within an order.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: fact_bookings  
**Source Column**: order_line_number  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Order Line Number  
**Data Type**: integer  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Line Number
- Line Item Number
- Order Line

---

## Related Concepts

### Related Entities
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Booking ID](booking-id.md)
- [Order Number](order-number.md)

---

## Usage Context

Order Line Number is used to:
- Identify specific items within an order
- Support line-level tracking
- Enable detailed order analysis

---

## Navigation

- [View Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Booking Transaction  
**Source Attribute**: Order Line Number  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
