---
title: Booking Transaction
type: glossary
description: Stores individual completed sales booking transactions with related financial measures and dimensional links
resource: glossary
tags: [booking, transaction, fact, sales, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Transaction

## Business Definition

Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions.

---

## Business Meaning

A booking transaction represents a completed sales event that generates revenue. It captures the financial details, quantities, and dimensional context of each sale, serving as the central fact entity for sales analysis.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking ID](./booking-id.md) - Unique identifier
- [Order Number](./order-number.md) - Business order reference
- [Booking Amount USD](./booking-amount-usd.md) - Revenue measure
- [Annual Contract Value USD](./annual-contract-value-usd.md) - Contract value measure
- [Customer](./customer.md) - Customer dimension
- [Product](./product.md) - Product dimension
- [Partner](./partner.md) - Partner dimension
- [Geography](./geography.md) - Geography dimension
- [Sales Representative](./sales-representative.md) - Sales representative dimension
- [Contract](./contract.md) - Contract dimension
- [Date](./date.md) - Date dimension

---

## Usage Context

Booking Transactions are used to:
- Record completed sales events
- Capture revenue and financial measures
- Link sales to dimensional context
- Enable multidimensional sales analysis

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
