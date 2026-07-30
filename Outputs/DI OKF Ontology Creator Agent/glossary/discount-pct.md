---
title: Discount Percentage
type: glossary
description: Discount applied to the booked item or service, stored as a fractional percentage of list price
resource: glossary
tags: [discount, percentage, pricing]
timestamp: 2024-01-15T00:00:00Z
---

# Discount Percentage

## Business Definition

Discount applied to the booked item or service, stored as a fractional percentage of list price. This represents the price reduction from the standard list price.

---

## Business Meaning

Discount Percentage represents the discount rate applied to reduce the list price. It is stored as a fractional value (e.g., 0.15 = 15% discount). The discount is used to calculate the final booking amount: booking_amount = (quantity × unit_list_price) × (1 - discount_pct). This metric is critical for analyzing pricing strategies, competitive pressure, and margin management.

---

## Technical Mapping

**Source Field**: bookings.discount_pct  
**Data Type**: Numeric (Decimal)  
**Unit**: Percentage (fractional, 0.0 to 1.0)

---

## Synonyms

- Discount Rate
- Discount Factor
- Price Discount
- Discount Applied

---

## Related Concepts

- [Unit List Price USD](unit-list-price-usd.md)
- [Booking Amount USD](booking-amount-usd.md)
- [Average Discount Percentage](../measures/average-discount-pct.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)

---

## Usage Context

Discount Percentage is used in:
- Calculating net booking amounts
- Analyzing discount trends
- Monitoring pricing effectiveness
- Assessing competitive pressure
- Margin analysis

---

## Navigation

- [Return to Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Average Discount Percentage Measure](../measures/average-discount-pct.md)
