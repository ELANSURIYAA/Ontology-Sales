---
title: Booking Amount USD
type: glossary
description: Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments
resource: glossary
tags: [booking, transaction, revenue, financial, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Amount USD

## Business Definition

Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments.

---

## Business Meaning

Booking Amount USD represents the actual revenue recognized from each booking transaction after applying discounts and pricing adjustments. This is the primary revenue metric for sales performance analysis.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Source Column:** booking_amount_usd  
**Data Type:** Numeric  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Attribute:** Booking Amount USD  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Parent entity
- [Unit List Price USD](./unit-list-price-usd.md) - Base price
- [Discount Percentage](./discount-percentage.md) - Discount applied
- [Quantity Sold](./quantity-sold.md) - Volume sold
- [Annual Contract Value USD](./annual-contract-value-usd.md) - Annualized value
- [Total Contract Value USD](./total-contract-value-usd.md) - Total value

---

## Usage Context

Booking Amount USD is used to:
- Track actual revenue from transactions
- Measure sales performance
- Calculate revenue metrics
- Support financial reporting

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [View Measure Definition](../measures/booking-amount-usd.md)
- [Return to Bundle Index](../index.md)
