---
title: Customer
type: entity
description: Business entity describing customer accounts that place orders and generate bookings.
resource: entities
tags: customer,entity,sales,bookings
timestamp: 2026-07-28T00:00:00Z
---

# Customer

## Business Definition

Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location.

---

## Technical Mapping

- Source Table: `QuoteToBooking.dim_customer`
- Domain: [Sales Bookings and Revenue Analytics](../domains/sales_bookings_and_revenue_analytics.md)

---

## Attributes

- Customer Key (`customer_key`) - integer - not nullable
- Customer ID (`customer_id`) - character varying(20) - not nullable
- Customer Name (`customer_name`) - character varying(80)
- Customer Segment (`segment`) - character varying(30)
- Industry (`industry`) - character varying(40)
- Account Tier (`account_tier`) - character varying(20)
- Headquarters Country (`hq_country`) - character varying(40)
- Headquarters Region (`hq_region`) - character varying(20)

---

## Primary Keys

- Customer Key

---

## Foreign Keys

None

---

## Measures

None

---

## Relationships

- [Customer to Booking Transaction](../relationships/customer_to_booking_transaction.md)

---

## Related Concepts

- [Customer](../glossary/customer.md)
- [Customer ID](../glossary/customer_id.md)
- [Customer Segment](../glossary/customer_segment.md)
- [Industry](../glossary/industry.md)
- [Account Tier](../glossary/account_tier.md)
- [Headquarters Country](../glossary/headquarters_country.md)
- [Headquarters Region](../glossary/headquarters_region.md)

---

## Business Rules

- Each customer record is uniquely identified by Customer Key.
- Customer ID is the business identifier assigned to the customer account.
- A customer can be associated with multiple booking transactions.

---

## Semantic Cross Links

- [Entities Index](index.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Booking Transaction](booking_transaction.md)
- [Customer to Booking Transaction](../relationships/customer_to_booking_transaction.md)
- [Glossary: Customer](../glossary/customer.md)
