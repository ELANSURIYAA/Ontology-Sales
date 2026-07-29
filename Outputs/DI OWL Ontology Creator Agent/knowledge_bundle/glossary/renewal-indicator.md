---
title: Renewal Indicator
type: glossary
description: Indicates whether the booking transaction is classified as a renewal
resource: glossary
tags: [booking, transaction, renewal, indicator, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Renewal Indicator

## Business Definition

Indicates whether the booking transaction is classified as a renewal.

---

## Business Meaning

Renewal Indicator is a binary flag that identifies whether a booking transaction represents a renewal of an existing customer contract. This metric is essential for tracking customer retention and recurring revenue.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Source Column:** is_renewal  
**Data Type:** Integer  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Attribute:** Renewal Indicator  
**Confidence Score:** 0.95

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Parent entity
- [Booking Type](./booking-type.md) - Booking classification
- [Auto Renew Flag](./auto-renew-flag.md) - Contract renewal behavior

---

## Usage Context

Renewal Indicator is used to:
- Identify renewal transactions
- Calculate renewal rates
- Track customer retention
- Analyze recurring revenue patterns

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
