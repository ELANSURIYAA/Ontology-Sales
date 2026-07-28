---
title: Booking Transaction
type: entity
description: Fact entity representing completed sales booking transactions and associated financial measures.
resource: entities
tags: [entity, booking-transaction, fact, revenue]
timestamp: 2026-07-28
---

# Booking Transaction

## Business Definition
Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions.

## Technical Mapping
- Source Table: `QuoteToBooking.fact_bookings`
- Related Glossary: [Booking Transaction](../glossary/booking-transaction.md)

## Attributes
- Booking ID
- Order Number
- Order Line Number
- Booking Date Key
- Customer Key
- Product Key
- Partner Key
- Geography Key
- Sales Representative Key
- Contract Key
- Booking Type
- Renewal Indicator
- Quantity Sold
- Unit List Price USD
- Discount Percentage
- Booking Amount USD
- Annual Contract Value USD
- Total Contract Value USD

## Primary Keys
- Booking ID

## Foreign Keys
- Booking Date Key
- Customer Key
- Product Key
- Partner Key
- Geography Key
- Sales Representative Key
- Contract Key

## Measures
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

## Relationships
- [Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)
- [Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)
- [Date to Booking Transaction](../relationships/date-to-booking-transaction.md)
- [Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)
- [Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)
- [Product to Booking Transaction](../relationships/product-to-booking-transaction.md)
- [Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)

## Related Concepts
- [Booking ID](../glossary/booking-id.md)
- [Order Number](../glossary/order-number.md)
- [Order Line Number](../glossary/order-line-number.md)
- [Booking Date Key](../glossary/booking-date-key.md)
- [Booking Type](../glossary/booking-type.md)
- [Renewal Indicator](../glossary/renewal-indicator.md)
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Contract](contract.md)
- [Customer](customer.md)
- [Date](date.md)
- [Geography](geography.md)
- [Partner](partner.md)
- [Product](product.md)
- [Sales Representative](sales-representative.md)

## Business Rules
- Each booking transaction is uniquely identified by Booking ID.
- Order Number and Order Line Number are additional business identifiers for transaction traceability.
- Booking transactions are classified as new sale or renewal through Booking Type and Renewal Indicator.
- Each booking transaction may reference contract, customer, date, geography, partner, product, and sales representative dimensions.
