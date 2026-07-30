---
title: Booking Amount USD
type: glossary
description: Total booked sales amount in US dollars after pricing and discount adjustments
resource: glossary
tags: [booking-amount, revenue, usd]
timestamp: 2024-01-15T00:00:00Z
---

# Booking Amount USD

## Business Definition

Total booked sales amount in US dollars after pricing and discount adjustments. This represents the net revenue value of the booking transaction.

---

## Business Meaning

Booking Amount USD is the final revenue value of a booking transaction after applying all pricing and discount adjustments. It is calculated as: (quantity × unit_list_price_usd) × (1 - discount_pct). This is the primary revenue metric at the transaction level and represents the actual revenue recognized from the booking.

---

## Technical Mapping

**Source Field**: bookings.booking_amount_usd  
**Data Type**: Numeric (Currency)  
**Unit**: USD

---

## Synonyms

- Booking Revenue
- Net Booking Amount
- Transaction Amount
- Sales Amount

---

## Related Concepts

- [Unit List Price USD](unit-list-price-usd.md)
- [Discount Percentage](discount-pct.md)
- [Quantity](quantity.md)
- [ACV USD](acv-usd.md)
- [TCV USD](tcv-usd.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)

---

## Usage Context

Booking Amount USD is used in:
- Calculating total revenue
- Analyzing transaction-level revenue
- Computing average booking values
- Revenue performance tracking
- Financial reporting

---

## Navigation

- [Return to Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Total Booking Amount USD Measure](../measures/total-booking-amount-usd.md)
