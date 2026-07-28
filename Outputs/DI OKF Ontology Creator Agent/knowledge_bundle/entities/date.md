---
title: Date
type: entity
description: Business entity describing calendar and fiscal dates used in booking analysis.
resource: entities
tags: date,entity,time,fiscal,sales
timestamp: 2026-07-28T00:00:00Z
---

# Date

## Business Definition

Stores calendar and fiscal date attributes used to analyze bookings over time.

---

## Technical Mapping

- Source Table: `QuoteToBooking.dim_date`
- Domain: [Sales Bookings and Revenue Analytics](../domains/sales_bookings_and_revenue_analytics.md)

---

## Attributes

- Date Key (`date_key`) - integer - not nullable
- Full Date (`full_date`) - date - not nullable
- Month Name (`month_name`) - character varying(12)
- Calendar Year (`calendar_year`) - integer
- Fiscal Year (`fiscal_year`) - character varying(6)
- Fiscal Quarter (`fiscal_quarter`) - character varying(10)
- Fiscal Period Sequence (`fiscal_period_seq`) - integer

---

## Primary Keys

- Date Key

---

## Foreign Keys

None

---

## Measures

None

---

## Relationships

- [Date to Booking Transaction](../relationships/date_to_booking_transaction.md)

---

## Related Concepts

- [Date](../glossary/date.md)
- [Date Key](../glossary/date_key.md)
- [Full Date](../glossary/full_date.md)
- [Month Name](../glossary/month_name.md)
- [Calendar Year](../glossary/calendar_year.md)
- [Fiscal Year](../glossary/fiscal_year.md)
- [Fiscal Quarter](../glossary/fiscal_quarter.md)
- [Fiscal Period Sequence](../glossary/fiscal_period_sequence.md)

---

## Business Rules

- Each date record is uniquely identified by Date Key.
- Date records support both calendar and fiscal reporting perspectives.
- A date can be associated with multiple booking transactions.

---

## Semantic Cross Links

- [Entities Index](index.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Booking Transaction](booking_transaction.md)
- [Date to Booking Transaction](../relationships/date_to_booking_transaction.md)
- [Glossary: Fiscal Year](../glossary/fiscal_year.md)
