---
title: Booking Transaction
type: entity
description: Individual completed sales booking transactions with financial measures, quantities, renewal status, and dimensional links
resource: entities
tags: [bookings, transactions, fact, sales, revenue]
timestamp: 2024-01-15T00:00:00Z
---

# Booking Transaction

## Business Definition

The Booking Transaction entity captures individual completed sales booking transactions and their associated financial measures, quantities, renewal status, and links to related business dimensions. This entity represents the atomic unit of analysis for sales performance and revenue analytics.

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings  
**Source Schema**: quotetobooking  
**Entity Type**: Fact  
**Grain**: One row per booking transaction

---

## Attributes

- booking_id
- order_number
- order_line_number
- date_key
- customer_key
- product_key
- partner_key
- geography_key
- sales_rep_key
- contract_key
- booking_type
- is_renewal
- quantity
- unit_list_price_usd
- discount_pct
- booking_amount_usd
- acv_usd
- tcv_usd

---

## Primary Keys

- booking_id

---

## Foreign Keys

- date_key → Date
- customer_key → Customer
- product_key → Product
- partner_key → Partner
- geography_key → Geography
- sales_rep_key → Sales Representative
- contract_key → Contract

---

## Relationships

- [Bookings to Contracts](../relationships/bookings-to-contracts.md)
- [Bookings to Customers](../relationships/bookings-to-customers.md)
- [Bookings to Dates](../relationships/bookings-to-dates.md)
- [Bookings to Geographies](../relationships/bookings-to-geographies.md)
- [Bookings to Partners](../relationships/bookings-to-partners.md)
- [Bookings to Products](../relationships/bookings-to-products.md)
- [Bookings to Sales Representatives](../relationships/bookings-to-sales-representatives.md)

---

## Measures

- [Booking Count](../measures/booking-count.md)
- [Distinct Order Count](../measures/distinct-order-count.md)
- [Total Quantity](../measures/total-quantity.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Average Discount Percentage](../measures/average-discount-pct.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

---

## Related Concepts

- [Booking Amount](../glossary/booking-amount-usd.md)
- [Annual Contract Value](../glossary/acv-usd.md)
- [Total Contract Value](../glossary/tcv-usd.md)
- [Booking Type](../glossary/booking-type.md)
- [Is Renewal](../glossary/is-renewal.md)
- [Quantity](../glossary/quantity.md)
- [Discount Percentage](../glossary/discount-pct.md)

---

## Business Rules

### Booking Amount Calculation
Booking amount is calculated as: (quantity × unit_list_price_usd) × (1 - discount_pct)

### Renewal Classification
Bookings are classified as renewal when is_renewal = 1, otherwise classified as net new business.

### ACV Calculation
Annual Contract Value represents the annualized value of the booking for subscription and recurring revenue analysis.

### TCV Calculation
Total Contract Value represents the full contract value over the entire term for multi-year deal analysis.

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Bookings Domain](../domains/bookings.md)
