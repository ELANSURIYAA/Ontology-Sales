---
title: Booking Transaction
type: glossary
description: Individual completed sales booking transactions with related financial measures and dimensional links
resource: glossary
tags: [glossary, booking, transaction, fact, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Transaction

## Business Definition

Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions.

---

## Business Meaning

A booking transaction represents a completed sale of products or services to a customer. Each transaction captures the financial details, quantities, pricing, and contextual information about who sold what to whom, when, where, and under what terms. Booking transactions are the fundamental unit of sales analysis and revenue measurement.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Confidence Score**: 1.00

---

## Related Concepts

- [Booking ID](booking-id.md)
- [Order Number](order-number.md)
- [Order Line Number](order-line-number.md)
- [Booking Date Key](booking-date-key.md)
- [Booking Type](booking-type.md)
- [Renewal Indicator](renewal-indicator.md)
- [Quantity Sold](quantity-sold.md)
- [Unit List Price USD](unit-list-price-usd.md)
- [Discount Percentage](discount-percentage.md)
- [Booking Amount USD](booking-amount-usd.md)
- [Annual Contract Value USD](annual-contract-value-usd.md)
- [Total Contract Value USD](total-contract-value-usd.md)

---

## Usage Context

Booking Transaction is used to:
- Record completed sales
- Enable revenue analysis
- Support sales performance measurement
- Facilitate financial reporting
- Enable multidimensional analysis

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
