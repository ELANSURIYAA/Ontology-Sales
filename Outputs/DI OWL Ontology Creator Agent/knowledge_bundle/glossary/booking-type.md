---
title: Booking Type
type: glossary
description: Indicates whether the booking is a new sale or a renewal
resource: glossary
tags: [booking, transaction, type, classification, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Type

## Business Definition

Indicates whether the booking is a new sale or a renewal.

---

## Business Meaning

Booking Type categorizes transactions as either new customer acquisitions or renewals of existing contracts. This classification is critical for analyzing new business growth versus customer retention performance.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Source Column:** booking_type  
**Data Type:** Character Varying(15)  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Attribute:** Booking Type  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Parent entity
- [Renewal Indicator](./renewal-indicator.md) - Binary renewal flag
- [Auto Renew Flag](./auto-renew-flag.md) - Contract renewal behavior

---

## Usage Context

Booking Type is used to:
- Categorize bookings as new or renewal
- Enable new vs renewal analysis
- Support growth and retention tracking
- Track booking mix by type

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
