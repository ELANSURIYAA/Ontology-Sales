---
title: Discount Percentage
type: glossary
description: Percentage discount applied to the list price for the booking transaction
resource: glossary
tags: [glossary, booking, discount, pricing, measure]
timestamp: 2026-07-28T00:00:00Z
---

# Discount Percentage

## Business Definition

Percentage discount applied to the list price for the booking transaction.

---

## Business Meaning

Discount Percentage represents the rate of price reduction applied to the standard list price. Discounts are negotiated based on factors such as deal size, customer relationship, competitive dynamics, and strategic importance. Discount percentage is a key metric for pricing strategy, margin management, and sales effectiveness analysis.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Source Column**: discount_pct

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Attribute**: Discount Percentage

**Data Type**: Numeric

**Confidence Score**: 1.00

---

## Related Concepts

- [Booking Transaction](booking-transaction.md)
- [Unit List Price USD](unit-list-price-usd.md)
- [Booking Amount USD](booking-amount-usd.md)
- [Quantity Sold](quantity-sold.md)

---

## Usage Context

Discount Percentage is used to:
- Measure pricing concessions
- Calculate discount amounts
- Support margin analysis
- Enable pricing strategy evaluation
- Facilitate discount trend analysis

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [View Measure: Discount Percentage](../measures/discount-percentage.md)
- [Back to Main Index](../index.md)
