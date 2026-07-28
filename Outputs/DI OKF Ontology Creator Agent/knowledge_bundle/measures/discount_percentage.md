---
title: Discount Percentage
type: measure
description: Measure representing the percentage discount applied to a booking transaction.
resource: measures
tags: discount percentage,measure,pricing,sales
timestamp: 2026-07-28T00:00:00Z
---

# Discount Percentage

## Business Definition

Percentage discount applied to the list price for the booking transaction.

---

## Formula

Derived directly from `QuoteToBooking.fact_bookings.discount_pct`.

---

## Aggregation

AVG

---

## Related Entities

- [Booking Transaction](../entities/booking_transaction.md)

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales_bookings_and_revenue_analytics.md)

---

## Semantic Cross Links

- [Measures Index](index.md)
- [Metrics](../metrics.md)
- [Booking Transaction](../entities/booking_transaction.md)
- [Glossary: Discount Percentage](../glossary/discount_percentage.md)
