---
title: Is Renewal
type: glossary
description: Indicator showing whether the booking transaction is a renewal
resource: glossary
tags: [is-renewal, flag, indicator, renewal]
timestamp: 2024-01-15T00:00:00Z
---

# Is Renewal

## Business Definition

Indicator showing whether the booking transaction is a renewal. This flag distinguishes renewal transactions from net new business.

---

## Business Meaning

Is Renewal is a boolean indicator that identifies whether a booking represents a renewal of an existing customer contract (value = 1) or net new business including new customer acquisitions and expansions (value = 0). This flag is critical for analyzing customer retention, recurring revenue, and business growth sources.

---

## Technical Mapping

**Source Field**: bookings.is_renewal  
**Data Type**: Boolean/Integer (0 or 1)  
**Dimension**: Yes

---

## Synonyms

- Renewal Flag
- Renewal Indicator
- Is Renewal Transaction

---

## Related Concepts

- [Booking Type](booking-type.md)
- [Booking Transaction](../entities/bookings.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

---

## Usage Context

Is Renewal is used in:
- Separating renewal from net new revenue
- Calculating renewal rates
- Analyzing customer retention
- Tracking recurring revenue health
- Business mix analysis

---

## Navigation

- [Return to Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Renewal Booking Amount USD Measure](../measures/renewal-booking-amount-usd.md)
- [View Net New Booking Amount USD Measure](../measures/net-new-booking-amount-usd.md)
