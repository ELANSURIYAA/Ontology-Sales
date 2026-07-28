---
title: Order Number
type: glossary
description: Business order number associated with the booking transaction
resource: glossary
tags: [glossary, booking, order, business-key]
timestamp: 2026-07-28T00:00:00Z
---

# Order Number

## Business Definition

Business order number associated with the booking transaction.

---

## Business Meaning

Order Number is the business-level identifier assigned to the customer order. It provides a human-readable reference for the booking transaction and is used in operational systems, customer communications, and order tracking.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: fact_bookings  
**Source Column**: order_number  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Order Number  
**Data Type**: character varying(20)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Order ID
- Purchase Order Number
- PO Number

---

## Related Concepts

### Related Entities
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Booking ID](booking-id.md)
- [Order Line Number](order-line-number.md)

---

## Usage Context

Order Number is used to:
- Reference orders in business operations
- Track order fulfillment
- Support customer service inquiries
- Link to order management systems

---

## Navigation

- [View Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Booking Transaction  
**Source Attribute**: Order Number  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
