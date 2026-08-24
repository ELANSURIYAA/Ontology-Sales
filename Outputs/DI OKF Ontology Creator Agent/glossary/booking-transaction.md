---
title: Booking Transaction
type: glossary
description: A completed sales transaction representing the commitment to purchase products or services
resource: glossary
tags: [booking, transaction, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Transaction

## Business Definition

A Booking Transaction is a completed sales transaction that represents a customer's commitment to purchase products or services. Each booking transaction is recorded at the order line level and captures the financial details, quantities, pricing, and dimensional attributes associated with the sale.

---

## Business Meaning

Booking transactions are the fundamental unit of analysis in the sales bookings and revenue analytics model. They represent confirmed sales that have been processed and recorded in the system, as opposed to quotes or opportunities that may not materialize into actual revenue.

Each booking transaction includes:
- Unique transaction identifier
- Sales order reference
- Customer information
- Product or service details
- Quantity and pricing
- Discount information
- Contract terms
- Geographic and temporal attributes
- Sales representative assignment
- Partner involvement

---

## Technical Mapping

**Source Entity**: [Bookings](../entities/bookings.md)

**Source Table**: quotetobooking.fact_bookings

**Primary Key**: booking_id

---

## Synonyms

- Booking
- Sales Booking
- Booking Record
- Booking Line
- Order Line

---

## Related Concepts

- [Sales Order](./sales-order.md) - Container for one or more booking transactions
- [Booking Amount](./booking-amount.md) - Revenue value of the booking
- [Annual Contract Value](./annual-contract-value.md) - Annualized value of the booking
- [Total Contract Value](./total-contract-value.md) - Total value over contract term
- [Renewal](./renewal.md) - Type of booking transaction
- [Net New Business](./net-new-business.md) - Type of booking transaction

---

## Related Entities

- [Bookings](../entities/bookings.md) - Fact table containing booking transactions
- [Customers](../entities/customers.md) - Customer associated with the booking
- [Products](../entities/products.md) - Product or service booked
- [Partners](../entities/partners.md) - Partner involved in the booking
- [Sales Representatives](../entities/sales-representatives.md) - Sales rep responsible for the booking
- [Contracts](../entities/contracts.md) - Contract terms for the booking
- [Dates](../entities/dates.md) - Date of the booking transaction

---

## Related Measures

- [Booking Count](../measures/booking-count.md) - Count of booking transactions
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md) - Total revenue from bookings
- [Average Booking Value USD](../measures/average-booking-value-usd.md) - Average value per booking

---

## Usage Context

Booking transactions are used for:
- Revenue tracking and reporting
- Sales performance analysis
- Quota attainment measurement
- Commission calculations
- Forecasting and planning
- Customer behavior analysis
- Product performance evaluation
- Channel effectiveness assessment

---

## Business Rules

1. Each booking transaction must have a unique booking_id
2. Booking transactions are recorded at the order line level
3. Each booking references exactly one customer, product, partner, sales rep, contract, geography, and date
4. Booking amounts must be non-negative
5. Booking transactions are immutable once recorded
6. Each booking is classified as either renewal or net new business

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
