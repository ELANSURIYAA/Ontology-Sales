---
title: Booking Transaction
type: entity
description: Transactional fact entity for completed sales bookings with pricing, quantity, contract value, and dimensional links.
resource: entities
tags: booking transaction,entity,fact,sales,revenue
timestamp: 2026-07-28T00:00:00Z
---

# Booking Transaction

## Business Definition

Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions.

---

## Technical Mapping

- Source Table: `QuoteToBooking.fact_bookings`
- Domain: [Sales Bookings and Revenue Analytics](../domains/sales_bookings_and_revenue_analytics.md)

---

## Attributes

- Booking ID (`booking_id`) - integer - not nullable
- Order Number (`order_number`) - character varying(20)
- Order Line Number (`order_line_number`) - integer
- Booking Date Key (`date_key`) - integer - foreign key
- Customer Key (`customer_key`) - integer - foreign key
- Product Key (`product_key`) - integer - foreign key
- Partner Key (`partner_key`) - integer - foreign key
- Geography Key (`geography_key`) - integer - foreign key
- Sales Representative Key (`sales_rep_key`) - integer - foreign key
- Contract Key (`contract_key`) - integer - foreign key
- Booking Type (`booking_type`) - character varying(15)
- Renewal Indicator (`is_renewal`) - integer
- Quantity Sold (`quantity`) - integer
- Unit List Price USD (`unit_list_price_usd`) - numeric
- Discount Percentage (`discount_pct`) - numeric
- Booking Amount USD (`booking_amount_usd`) - numeric
- Annual Contract Value USD (`acv_usd`) - numeric
- Total Contract Value USD (`tcv_usd`) - numeric

---

## Primary Keys

- Booking ID

---

## Foreign Keys

- Booking Date Key -> [Date](date.md)
- Customer Key -> [Customer](customer.md)
- Product Key -> [Product](product.md)
- Partner Key -> [Partner](partner.md)
- Geography Key -> [Geography](geography.md)
- Sales Representative Key -> [Sales Representative](sales_representative.md)
- Contract Key -> [Contract](contract.md)

---

## Measures

- [Quantity Sold](../measures/quantity_sold.md)
- [Unit List Price USD](../measures/unit_list_price_usd.md)
- [Discount Percentage](../measures/discount_percentage.md)
- [Booking Amount USD](../measures/booking_amount_usd.md)
- [Annual Contract Value USD](../measures/annual_contract_value_usd.md)
- [Total Contract Value USD](../measures/total_contract_value_usd.md)

---

## Relationships

- [Contract to Booking Transaction](../relationships/contract_to_booking_transaction.md)
- [Customer to Booking Transaction](../relationships/customer_to_booking_transaction.md)
- [Date to Booking Transaction](../relationships/date_to_booking_transaction.md)
- [Geography to Booking Transaction](../relationships/geography_to_booking_transaction.md)
- [Partner to Booking Transaction](../relationships/partner_to_booking_transaction.md)
- [Product to Booking Transaction](../relationships/product_to_booking_transaction.md)
- [Sales Representative to Booking Transaction](../relationships/sales_representative_to_booking_transaction.md)

---

## Related Concepts

- [Booking Transaction](../glossary/booking_transaction.md)
- [Booking ID](../glossary/booking_id.md)
- [Order Number](../glossary/order_number.md)
- [Order Line Number](../glossary/order_line_number.md)
- [Booking Type](../glossary/booking_type.md)
- [Renewal Indicator](../glossary/renewal_indicator.md)
- [Booking Amount USD](../glossary/booking_amount_usd.md)

---

## Business Rules

- Each booking transaction record is uniquely identified by Booking ID.
- The fact record links to one date, customer, product, partner, geography, sales representative, and contract context.
- Booking transactions support quantity, list price, discount, booked revenue, annual contract value, and total contract value analysis.
- Booking Type indicates whether the booking is a new sale or a renewal.

---

## Semantic Cross Links

- [Entities Index](index.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Metrics](../metrics.md)
- [Booking Amount USD](../measures/booking_amount_usd.md)
- [Customer](customer.md)
- [Product](product.md)
