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

Renewal Indicator is a binary flag that identifies whether a booking transaction represents a renewal of an existing subscription or contract. This indicator enables precise measurement of renewal rates, customer retention, and recurring revenue. It complements the Booking Type attribute by providing a numeric flag for efficient filtering and calculation.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Source Column**: is_renewal

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Attribute**: Renewal Indicator

**Data Type**: Integer

**Confidence Score**: 0.95

---

## Related Concepts

- [Booking Transaction](booking-transaction.md)
- [Booking Type](booking-type.md)
- [Auto Renew Flag](auto-renew-flag.md)

---

## Usage Context

Renewal Indicator is used to:
- Identify renewal transactions
- Calculate renewal rates
- Measure customer retention
- Support recurring revenue analysis
- Enable new vs. renewal filtering

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
