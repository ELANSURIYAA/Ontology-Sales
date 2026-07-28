---
title: Booking Transaction
type: glossary
description: Individual completed sales booking transactions with related financial measures and links to dimensions
resource: glossary
tags: [glossary, booking, transaction, fact, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Transaction

## Business Definition

Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions.

---

## Business Meaning

A booking transaction represents a completed sales order that has been recorded in the system. It captures the details of what was sold, to whom, by whom, when, where, and for how much. Booking transactions are the fundamental unit of sales analysis and serve as the basis for revenue reporting, sales performance tracking, and business analytics.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: fact_bookings  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Confidence Score**: 1.00

---

## Synonyms

- Booking
- Sales Transaction
- Order
- Sales Booking

---

## Related Concepts

### Related Entities
- [Booking Transaction](../entities/booking-transaction.md)
- [Contract](../entities/contract.md)
- [Customer](../entities/customer.md)
- [Date](../entities/date.md)
- [Geography](../entities/geography.md)
- [Partner](../entities/partner.md)
- [Product](../entities/product.md)
- [Sales Representative](../entities/sales-representative.md)

### Related Attributes
- [Booking ID](booking-id.md)
- [Order Number](order-number.md)
- [Order Line Number](order-line-number.md)
- [Booking Date Key](booking-date-key.md)
- [Booking Type](booking-type.md)
- [Renewal Indicator](renewal-indicator.md)

### Related Measures
- [Quantity Sold](quantity-sold.md)
- [Unit List Price USD](unit-list-price-usd.md)
- [Discount Percentage](discount-percentage.md)
- [Booking Amount USD](booking-amount-usd.md)
- [Annual Contract Value USD](annual-contract-value-usd.md)
- [Total Contract Value USD](total-contract-value-usd.md)

---

## Usage Context

Booking Transactions are used to:
- Record completed sales
- Track revenue and performance
- Analyze sales patterns
- Support financial reporting

---

## Navigation

- [View Glossary Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Entity  
**Source Entity**: Booking Transaction  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
