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

Booking Type classifies booking transactions as either new sales (first-time purchases from new or existing customers) or renewals (repeat purchases of existing subscriptions or contracts). This classification is critical for understanding customer acquisition vs. retention dynamics, measuring renewal rates, and forecasting recurring revenue.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Source Column**: booking_type

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Attribute**: Booking Type

**Data Type**: Character Varying(15)

**Confidence Score**: 1.00

---

## Related Concepts

- [Booking Transaction](booking-transaction.md)
- [Renewal Indicator](renewal-indicator.md)
- [Auto Renew Flag](auto-renew-flag.md)

---

## Usage Context

Booking Type is used to:
- Classify bookings as new or renewal
- Enable new vs. renewal analysis
- Support renewal rate calculation
- Facilitate customer retention measurement
- Enable revenue mix analysis

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
