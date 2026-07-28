---
title: Booking ID
type: glossary
description: Unique identifier for an individual booking transaction record
resource: glossary
tags: [glossary, booking, identifier, primary-key]
timestamp: 2026-07-28T00:00:00Z
---

# Booking ID

## Business Definition

Unique identifier for an individual booking transaction record.

---

## Business Meaning

Booking ID is the system-generated unique identifier that distinguishes each booking transaction. It serves as the primary key for the booking transaction fact table and ensures that each sales transaction can be uniquely identified and tracked throughout the system.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: fact_bookings  
**Source Column**: booking_id  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Booking ID  
**Data Type**: integer  
**Nullable**: No  
**Primary Key**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Transaction ID
- Booking Identifier
- Booking Record ID

---

## Related Concepts

### Related Entities
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Order Number](order-number.md)
- [Order Line Number](order-line-number.md)

---

## Usage Context

Booking ID is used to:
- Uniquely identify booking transactions
- Support transaction-level analysis
- Enable drill-down to transaction details
- Maintain data integrity

---

## Navigation

- [View Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Booking Transaction  
**Source Attribute**: Booking ID  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
