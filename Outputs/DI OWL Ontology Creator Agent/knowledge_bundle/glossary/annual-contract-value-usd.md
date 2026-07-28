---
title: Annual Contract Value USD
type: glossary
description: Annualized value of the contract associated with the booking in U.S. dollars
resource: glossary
tags: [glossary, booking, acv, contract-value, measure]
timestamp: 2026-07-28T00:00:00Z
---

# Annual Contract Value USD

## Business Definition

Annualized value of the contract associated with the booking in U.S. dollars.

---

## Business Meaning

Annual Contract Value (ACV) represents the normalized annual value of a contract, regardless of its actual term length. For multi-year contracts, ACV divides the total contract value by the number of years to provide a consistent annual metric. ACV is critical for subscription business models, recurring revenue forecasting, and year-over-year growth measurement. All amounts are recorded in U.S. dollars.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Source Column**: acv_usd

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Attribute**: Annual Contract Value USD

**Data Type**: Numeric

**Confidence Score**: 1.00

---

## Related Concepts

- [Booking Transaction](booking-transaction.md)
- [Booking Amount USD](booking-amount-usd.md)
- [Total Contract Value USD](total-contract-value-usd.md)
- [Contract Term Months](contract-term-months.md)

---

## Usage Context

Annual Contract Value USD is used to:
- Measure recurring revenue
- Support subscription business analysis
- Enable year-over-year comparisons
- Facilitate revenue forecasting
- Calculate customer lifetime value

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [View Measure: Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Back to Main Index](../index.md)
