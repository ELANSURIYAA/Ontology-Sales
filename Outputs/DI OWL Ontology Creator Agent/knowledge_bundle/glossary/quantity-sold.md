---
title: Quantity Sold
type: glossary
description: Number of units, licenses, or subscriptions included in the booking transaction
resource: glossary
tags: [glossary, booking, quantity, volume, measure]
timestamp: 2026-07-28T00:00:00Z
---

# Quantity Sold

## Business Definition

Number of units, licenses, or subscriptions included in the booking transaction.

---

## Business Meaning

Quantity Sold represents the volume of items purchased in a booking transaction. Depending on the product type, this may represent physical units (hardware), software licenses, or subscription seats. Quantity is a key measure for volume analysis, capacity planning, and pricing calculations.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Source Column**: quantity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Attribute**: Quantity Sold

**Data Type**: Integer

**Confidence Score**: 1.00

---

## Related Concepts

- [Booking Transaction](booking-transaction.md)
- [Unit List Price USD](unit-list-price-usd.md)
- [Booking Amount USD](booking-amount-usd.md)

---

## Usage Context

Quantity Sold is used to:
- Measure volume of sales
- Calculate total units sold
- Support capacity planning
- Enable pricing calculations
- Facilitate volume-based analysis

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [View Measure: Quantity Sold](../measures/quantity-sold.md)
- [Back to Main Index](../index.md)
