---
title: Total Contract Value USD
type: glossary
description: Total value of the full contract associated with the booking in U.S. dollars
resource: glossary
tags: [glossary, booking, tcv, contract-value, measure]
timestamp: 2026-07-28T00:00:00Z
---

# Total Contract Value USD

## Business Definition

Total value of the full contract associated with the booking in U.S. dollars.

---

## Business Meaning

Total Contract Value (TCV) represents the complete financial commitment of a contract over its entire term. Unlike ACV which normalizes to annual values, TCV captures the full multi-year value of customer commitments. TCV is essential for measuring total deal size, customer commitment levels, and long-term revenue potential. All amounts are recorded in U.S. dollars.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Source Column**: tcv_usd

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Attribute**: Total Contract Value USD

**Data Type**: Numeric

**Confidence Score**: 1.00

---

## Related Concepts

- [Booking Transaction](booking-transaction.md)
- [Booking Amount USD](booking-amount-usd.md)
- [Annual Contract Value USD](annual-contract-value-usd.md)
- [Contract Term Months](contract-term-months.md)

---

## Usage Context

Total Contract Value USD is used to:
- Measure total contract commitments
- Support deal size analysis
- Enable customer commitment measurement
- Facilitate pipeline value tracking
- Calculate total revenue potential

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [View Measure: Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Back to Main Index](../index.md)
