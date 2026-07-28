---
title: Geography
type: entity
description: Business entity describing reporting geography for sales bookings.
resource: entities
tags: geography,entity,region,country,sales
timestamp: 2026-07-28T00:00:00Z
---

# Geography

## Business Definition

Stores geographic attributes used to analyze bookings by sales region, theater, and country.

---

## Technical Mapping

- Source Table: `QuoteToBooking.dim_geography`
- Domain: [Sales Bookings and Revenue Analytics](../domains/sales_bookings_and_revenue_analytics.md)

---

## Attributes

- Geography Key (`geography_key`) - integer - not nullable
- Sales Region (`region`) - character varying(20)
- Sales Theater (`theater`) - character varying(30)
- Country (`country`) - character varying(40)

---

## Primary Keys

- Geography Key

---

## Foreign Keys

None

---

## Measures

None

---

## Relationships

- [Geography to Booking Transaction](../relationships/geography_to_booking_transaction.md)

---

## Related Concepts

- [Geography](../glossary/geography.md)
- [Geography Key](../glossary/geography_key.md)
- [Sales Region](../glossary/sales_region.md)
- [Sales Theater](../glossary/sales_theater.md)
- [Country](../glossary/country.md)

---

## Business Rules

- Each geography record is uniquely identified by Geography Key.
- Geography supports analysis by region, theater, and country.
- A geography can be associated with multiple booking transactions.

---

## Semantic Cross Links

- [Entities Index](index.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Booking Transaction](booking_transaction.md)
- [Geography to Booking Transaction](../relationships/geography_to_booking_transaction.md)
- [Glossary: Geography](../glossary/geography.md)
