---
title: Unit List Price USD
type: glossary
description: Standard list price per unit in U.S. dollars before discounts are applied
resource: glossary
tags: [booking, transaction, price, pricing, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Unit List Price USD

## Business Definition

Standard list price per unit in U.S. dollars before discounts are applied.

---

## Business Meaning

Unit List Price USD represents the published standard price for a product or service unit before any discounts or pricing adjustments. This measure is essential for pricing analysis and discount effectiveness evaluation.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Source Column:** unit_list_price_usd  
**Data Type:** Numeric  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Attribute:** Unit List Price USD  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Parent entity
- [Quantity Sold](./quantity-sold.md) - Volume sold
- [Discount Percentage](./discount-percentage.md) - Discount applied
- [Booking Amount USD](./booking-amount-usd.md) - Final revenue

---

## Usage Context

Unit List Price USD is used to:
- Define standard product pricing
- Calculate potential revenue
- Analyze discount impact
- Support pricing strategy

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [View Measure Definition](../measures/unit-list-price-usd.md)
- [Return to Bundle Index](../index.md)
