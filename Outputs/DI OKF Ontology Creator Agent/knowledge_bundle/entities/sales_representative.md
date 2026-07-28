---
title: Sales Representative
type: entity
description: Business entity describing sales personnel responsible for customer relationships and bookings.
resource: entities
tags: sales representative,entity,sales,coverage
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative

## Business Definition

Stores information about sales personnel responsible for managing customer relationships and booking transactions.

---

## Technical Mapping

- Source Table: `QuoteToBooking.dim_sales_rep`
- Domain: [Sales Bookings and Revenue Analytics](../domains/sales_bookings_and_revenue_analytics.md)

---

## Attributes

- Sales Representative Key (`sales_rep_key`) - integer - not nullable
- Sales Representative ID (`rep_id`) - character varying(20) - not nullable
- Sales Representative Name (`rep_name`) - character varying(60)
- Sales Role (`sales_role`) - character varying(40)
- Sales Team (`sales_team`) - character varying(40)
- Covered Segment (`segment_covered`) - character varying(30)

---

## Primary Keys

- Sales Representative Key

---

## Foreign Keys

None

---

## Measures

None

---

## Relationships

- [Sales Representative to Booking Transaction](../relationships/sales_representative_to_booking_transaction.md)

---

## Related Concepts

- [Sales Representative](../glossary/sales_representative.md)
- [Sales Representative ID](../glossary/sales_representative_id.md)
- [Sales Representative Name](../glossary/sales_representative_name.md)
- [Sales Role](../glossary/sales_role.md)
- [Sales Team](../glossary/sales_team.md)
- [Covered Segment](../glossary/covered_segment.md)

---

## Business Rules

- Each sales representative record is uniquely identified by Sales Representative Key.
- Sales Representative ID is the business identifier assigned to the sales representative.
- A sales representative can be associated with multiple booking transactions.

---

## Semantic Cross Links

- [Entities Index](index.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Booking Transaction](booking_transaction.md)
- [Sales Representative to Booking Transaction](../relationships/sales_representative_to_booking_transaction.md)
- [Glossary: Sales Role](../glossary/sales_role.md)
