---
title: Quantity Sold
type: measure
description: Measure representing the number of units, licenses, or subscriptions included in a booking transaction.
resource: measures
tags: quantity sold,measure,bookings,sales
timestamp: 2026-07-28T00:00:00Z
---

# Quantity Sold

## Business Definition

Number of units, licenses, or subscriptions included in the booking transaction.

---

## Formula

Derived directly from `QuoteToBooking.fact_bookings.quantity`.

---

## Aggregation

SUM

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
- [Glossary: Quantity Sold](../glossary/quantity_sold.md)
