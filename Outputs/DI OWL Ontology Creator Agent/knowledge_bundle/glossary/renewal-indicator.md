---
title: Renewal Indicator
type: glossary
description: Indicates whether the booking transaction is classified as a renewal
resource: glossary
tags: [glossary, booking, renewal, indicator, flag]
timestamp: 2026-07-28T00:00:00Z
---

# Renewal Indicator

## Business Definition

Indicates whether the booking transaction is classified as a renewal.

---

## Business Meaning

Renewal Indicator is a binary flag that identifies whether a booking represents a renewal of an existing customer relationship or contract. Renewal tracking is essential for measuring customer retention, calculating renewal rates, and forecasting recurring revenue.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: fact_bookings  
**Source Column**: is_renewal  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Renewal Indicator  
**Data Type**: integer  
**Nullable**: Yes  
**Confidence Score**: 0.95

---

## Synonyms

- Is Renewal
- Renewal Flag
- Renewal Status

---

## Related Concepts

### Related Entities
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Booking Type](booking-type.md)
- [Auto Renew Flag](auto-renew-flag.md)

---

## Usage Context

Renewal Indicator is used to:
- Identify renewal transactions
- Calculate renewal rates
- Track customer retention
- Forecast recurring revenue

---

## Examples

- 1 (Yes - is a renewal)
- 0 (No - not a renewal)

---

## Navigation

- [View Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Booking Transaction  
**Source Attribute**: Renewal Indicator  
**Confidence Score**: 0.95  
**Last Updated**: 2026-07-28T00:00:00Z
