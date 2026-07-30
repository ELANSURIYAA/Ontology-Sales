---
title: Quantity
type: glossary
description: Number of units, licenses, or services booked in the transaction
resource: glossary
tags: [quantity, units, licenses, volume]
timestamp: 2024-01-15T00:00:00Z
---

# Quantity

## Business Definition

Number of units, licenses, or services booked in the transaction. This measure represents the volume of items purchased.

---

## Business Meaning

Quantity represents the number of units, licenses, or services included in a booking transaction. It is used to calculate total volume sold, average selling price per unit, and unit-based metrics. Quantity is particularly important for products sold by count (e.g., software licenses, hardware units, service subscriptions).

---

## Technical Mapping

**Source Field**: bookings.quantity  
**Data Type**: Numeric  
**Unit**: Units/Licenses

---

## Synonyms

- Units
- License Count
- Volume
- Item Count

---

## Related Concepts

- [Unit List Price USD](unit-list-price-usd.md)
- [Booking Amount USD](booking-amount-usd.md)
- [Total Quantity](../measures/total-quantity.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)

---

## Usage Context

Quantity is used in:
- Calculating total units sold
- Computing average selling price per unit
- Analyzing product adoption rates
- Tracking license deployment
- Volume-based analysis

---

## Navigation

- [Return to Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Total Quantity Measure](../measures/total-quantity.md)
