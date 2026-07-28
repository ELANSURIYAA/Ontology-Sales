---
title: Booking Amount USD
type: glossary
description: Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments
resource: glossary
tags: [glossary, booking, revenue, amount, measure]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Amount USD

## Business Definition

Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments.

---

## Business Meaning

Booking Amount USD is the primary revenue metric representing the net value of a completed booking transaction after all pricing adjustments, discounts, and negotiations. This is the actual revenue recognized from the sale and serves as the foundation for financial reporting, performance measurement, and revenue forecasting. All amounts are recorded in U.S. dollars for consistent financial analysis.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Source Column**: booking_amount_usd

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Attribute**: Booking Amount USD

**Data Type**: Numeric

**Confidence Score**: 1.00

---

## Related Concepts

- [Booking Transaction](booking-transaction.md)
- [Unit List Price USD](unit-list-price-usd.md)
- [Discount Percentage](discount-percentage.md)
- [Quantity Sold](quantity-sold.md)
- [Annual Contract Value USD](annual-contract-value-usd.md)
- [Total Contract Value USD](total-contract-value-usd.md)

---

## Usage Context

Booking Amount USD is used to:
- Measure total revenue
- Support financial reporting
- Enable performance measurement
- Facilitate revenue forecasting
- Calculate key revenue metrics

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [View Measure: Booking Amount USD](../measures/booking-amount-usd.md)
- [Back to Main Index](../index.md)
