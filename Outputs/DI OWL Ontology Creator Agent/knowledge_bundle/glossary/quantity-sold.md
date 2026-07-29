---
title: Quantity Sold
type: glossary
description: Number of units, licenses, or subscriptions included in the booking transaction
resource: glossary
tags: [booking, transaction, quantity, volume, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Quantity Sold

## Business Definition

Number of units, licenses, or subscriptions included in the booking transaction.

---

## Business Meaning

Quantity Sold represents the volume of products or services sold in each transaction. This measure is essential for volume analysis, capacity planning, and understanding product demand patterns.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Source Column:** quantity  
**Data Type:** Integer  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Attribute:** Quantity Sold  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Parent entity
- [Unit List Price USD](./unit-list-price-usd.md) - Price per unit
- [Booking Amount USD](./booking-amount-usd.md) - Total revenue

---

## Usage Context

Quantity Sold is used to:
- Track volume of products sold
- Calculate average selling prices
- Support capacity and demand planning
- Enable volume-based analysis

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [View Measure Definition](../measures/quantity-sold.md)
- [Return to Bundle Index](../index.md)
