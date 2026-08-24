---
title: Booking Transaction
type: glossary
description: Individual completed sales booking event representing a customer purchase
resource: glossary
tags: [booking, transaction, sales, event]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Transaction

## Business Definition

An individual completed sales booking event representing a customer purchase of products or services.

A booking transaction is the fundamental unit of sales activity, capturing the details of what was sold, to whom, when, and under what terms.

---

## Business Meaning

Booking transactions represent confirmed sales orders that have been processed and recorded in the sales system. Each transaction captures:
- The customer making the purchase
- The products or services being purchased
- The quantity and pricing
- The sales channel and representative
- The contract terms and duration
- The geographic territory
- The timing of the transaction

Booking transactions form the basis for all sales performance analysis, revenue recognition, and forecasting activities.

---

## Technical Mapping

**Source Entity**: [Bookings](../entities/bookings.md)

**Source Table**: quotetobooking.fact_bookings

**Primary Key**: booking_id

---

## Synonyms

- Sales booking
- Booking event
- Sales transaction
- Order booking
- Completed booking

---

## Related Concepts

- [Annual Contract Value](annual-contract-value.md)
- [Total Contract Value](total-contract-value.md)
- [Renewal](renewal.md)
- [Net New Business](net-new-business.md)

---

## Related Entities

- [Bookings](../entities/bookings.md)
- [Customers](../entities/customers.md)
- [Products](../entities/products.md)
- [Contracts](../entities/contracts.md)

---

## Related Measures

- [Booking Count](../measures/booking-count.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

---

## Usage Examples

- "Analyze booking transactions by customer segment"
- "Track booking transaction volume over time"
- "Calculate average booking transaction value"
- "Identify high-value booking transactions"

---

## Navigation

- [Return to Glossary Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
