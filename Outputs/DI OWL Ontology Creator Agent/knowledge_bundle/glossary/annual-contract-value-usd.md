---
title: Annual Contract Value USD
type: glossary
description: Annualized value of the contract associated with the booking in U.S. dollars
resource: glossary
tags: [booking, transaction, contract, acv, financial, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Annual Contract Value USD

## Business Definition

Annualized value of the contract associated with the booking in U.S. dollars.

---

## Business Meaning

Annual Contract Value USD represents the yearly value of a contract, normalizing multi-year agreements to an annual basis for consistent comparison and analysis. This metric is essential for subscription and recurring revenue analysis.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Source Column:** acv_usd  
**Data Type:** Numeric  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Attribute:** Annual Contract Value USD  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Parent entity
- [Total Contract Value USD](./total-contract-value-usd.md) - Total contract value
- [Booking Amount USD](./booking-amount-usd.md) - Initial booking revenue
- [Contract Term Months](./contract-term-months.md) - Contract duration

---

## Usage Context

Annual Contract Value USD is used to:
- Track annual recurring revenue
- Compare contracts of different lengths
- Forecast annual revenue
- Analyze subscription performance

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [View Measure Definition](../measures/annual-contract-value-usd.md)
- [Return to Bundle Index](../index.md)
