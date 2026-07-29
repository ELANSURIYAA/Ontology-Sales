---
title: Discount Percentage
type: glossary
description: Percentage discount applied to the list price for the booking transaction
resource: glossary
tags: [booking, transaction, discount, pricing, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Discount Percentage

## Business Definition

Percentage discount applied to the list price for the booking transaction.

---

## Business Meaning

Discount Percentage represents the pricing concession given to customers, expressed as a percentage of the list price. This measure is critical for margin analysis and pricing strategy evaluation.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Source Column:** discount_pct  
**Data Type:** Numeric  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Attribute:** Discount Percentage  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Parent entity
- [Unit List Price USD](./unit-list-price-usd.md) - Base price
- [Booking Amount USD](./booking-amount-usd.md) - Final revenue after discount

---

## Usage Context

Discount Percentage is used to:
- Track pricing concessions
- Analyze discount patterns
- Evaluate margin impact
- Support pricing optimization

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [View Measure Definition](../measures/discount-percentage.md)
- [Return to Bundle Index](../index.md)
