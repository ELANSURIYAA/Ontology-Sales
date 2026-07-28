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

Booking ID is the unique identifier that distinguishes each individual booking transaction in the system. It serves as the primary key for booking records and enables precise transaction tracking, auditing, and reference. Each booking transaction has exactly one Booking ID that remains constant throughout its lifecycle.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Source Column**: booking_id

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Attribute**: Booking ID

**Data Type**: Integer

**Confidence Score**: 1.00

---

## Related Concepts

- [Booking Transaction](booking-transaction.md)
- [Order Number](order-number.md)
- [Order Line Number](order-line-number.md)

---

## Usage Context

Booking ID is used to:
- Uniquely identify booking transactions
- Support transaction tracking and auditing
- Enable transaction-level analysis
- Facilitate data quality verification
- Support transaction reconciliation

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
