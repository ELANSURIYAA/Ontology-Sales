---
title: Booking Type
type: glossary
description: Indicates whether the booking is a new sale or a renewal
resource: glossary
tags: [glossary, booking, type, classification]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Type

## Business Definition

Indicates whether the booking is a new sale or a renewal.

---

## Business Meaning

Booking Type classifies transactions as either new business or renewal business. This distinction is critical for understanding revenue composition, tracking customer retention, and measuring new customer acquisition versus existing customer expansion.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: fact_bookings  
**Source Column**: booking_type  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Booking Type  
**Data Type**: character varying(15)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Transaction Type
- Sale Type

---

## Related Concepts

### Related Entities
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Renewal Indicator](renewal-indicator.md)

---

## Usage Context

Booking Type is used to:
- Distinguish new vs renewal revenue
- Track customer retention
- Analyze revenue composition

---

## Examples

- New
- Renewal

---

## Navigation

- [View Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Booking Transaction  
**Source Attribute**: Booking Type  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
