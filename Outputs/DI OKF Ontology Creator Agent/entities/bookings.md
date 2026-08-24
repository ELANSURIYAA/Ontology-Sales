---
title: Bookings
type: entity
description: Individual completed sales booking transactions with financial measures and dimensional links
resource: entities
tags: [bookings, transactions, fact, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings

## Business Definition

Captures individual completed sales booking transactions and their associated financial measures, quantities, renewal status, and links to related business dimensions.

This is the central fact entity in the sales bookings and revenue analytics model, representing the grain of analysis at the individual booking transaction level.

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings

**Source Columns**: booking_id, order_number, order_line_number, date_key, customer_key, product_key, partner_key, geography_key, sales_rep_key, contract_key, booking_type, is_renewal, quantity, unit_list_price_usd, discount_pct, booking_amount_usd, acv_usd, tcv_usd

---

## Attributes

- **booking_id** - Unique identifier for an individual booking transaction record
- **order_number** - Sales order number associated with the booking transaction
- **order_line_number** - Line number within the sales order representing the booked item or service
- **date_key** - Foreign key linking the booking transaction to the reporting date dimension
- **customer_key** - Foreign key linking the booking transaction to the customer dimension
- **product_key** - Foreign key linking the booking transaction to the product dimension
- **partner_key** - Foreign key linking the booking transaction to the partner dimension
- **geography_key** - Foreign key linking the booking transaction to the geography dimension
- **sales_rep_key** - Foreign key linking the booking transaction to the sales representative dimension
- **contract_key** - Foreign key linking the booking transaction to the contract dimension
- **booking_type** - Type of booking event, such as new business or renewal
- **is_renewal** - Indicator showing whether the booking transaction is a renewal
- **quantity** - Number of units, licenses, or services booked in the transaction
- **unit_list_price_usd** - Standard list price per unit in US dollars before discounts
- **discount_pct** - Discount applied to the booked item or service, stored as a fractional percentage of list price
- **booking_amount_usd** - Total booked sales amount in US dollars after pricing and discount adjustments
- **acv_usd** - Annualized contract value of the booking in US dollars
- **tcv_usd** - Total contract value of the booking over the full contract term in US dollars

---

## Primary Keys

- booking_id

---

## Foreign Keys

- date_key → [Dates](dates.md)
- customer_key → [Customers](customers.md)
- product_key → [Products](products.md)
- partner_key → [Partners](partners.md)
- geography_key → [Geographies](geographies.md)
- sales_rep_key → [Sales Representatives](sales-representatives.md)
- contract_key → [Contracts](contracts.md)

---

## Relationships

- [Bookings to Dates](../relationships/bookings-to-dates.md)
- [Bookings to Customers](../relationships/bookings-to-customers.md)
- [Bookings to Products](../relationships/bookings-to-products.md)
- [Bookings to Partners](../relationships/bookings-to-partners.md)
- [Bookings to Geographies](../relationships/bookings-to-geographies.md)
- [Bookings to Sales Representatives](../relationships/bookings-to-sales-representatives.md)
- [Bookings to Contracts](../relationships/bookings-to-contracts.md)

---

## Measures

- [Booking Count](../measures/booking-count.md)
- [Distinct Order Count](../measures/distinct-order-count.md)
- [Total Quantity](../measures/total-quantity.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Average Discount Pct](../measures/average-discount-pct.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

---

## Related Concepts

- [Booking Transaction](../glossary/booking-transaction.md)
- [Annual Contract Value](../glossary/annual-contract-value.md)
- [Total Contract Value](../glossary/total-contract-value.md)
- [Renewal](../glossary/renewal.md)
- [Net New Business](../glossary/net-new-business.md)

---

## Business Rules

- Each booking transaction must have a unique booking_id
- Booking transactions must be linked to valid dimension records via foreign keys
- booking_amount_usd represents the net revenue after discounts
- is_renewal flag determines classification as renewal vs net new business
- ACV and TCV values are calculated based on contract terms and booking amounts

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
