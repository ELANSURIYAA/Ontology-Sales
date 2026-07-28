---
title: Contract
type: entity
description: Business entity describing commercial agreements associated with bookings.
resource: entities
tags: contract,entity,sales,bookings
timestamp: 2026-07-28T00:00:00Z
---

# Contract

## Business Definition

Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level.

---

## Technical Mapping

- Source Table: `QuoteToBooking.dim_contract`
- Domain: [Sales Bookings and Revenue Analytics](../domains/sales_bookings_and_revenue_analytics.md)

---

## Attributes

- Contract Key (`contract_key`) - integer - not nullable
- Contract Type (`contract_type`) - character varying(40)
- Contract Term Months (`term_months`) - integer
- Auto Renew Flag (`auto_renew_flag`) - character(1)
- Coverage Level (`coverage_level`) - character varying(20)

---

## Primary Keys

- Contract Key

---

## Foreign Keys

None

---

## Measures

None

---

## Relationships

- [Contract to Booking Transaction](../relationships/contract_to_booking_transaction.md)

---

## Related Concepts

- [Contract](../glossary/contract.md)
- [Contract Type](../glossary/contract_type.md)
- [Contract Term Months](../glossary/contract_term_months.md)
- [Auto Renew Flag](../glossary/auto_renew_flag.md)
- [Coverage Level](../glossary/coverage_level.md)

---

## Business Rules

- Each contract record is uniquely identified by Contract Key.
- Contract records may classify agreement structure, term duration, renewal behavior, and support coverage used in booking analysis.
- A contract can relate to multiple booking transactions through the booking fact.

---

## Semantic Cross Links

- [Entities Index](index.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Booking Transaction](booking_transaction.md)
- [Contract to Booking Transaction](../relationships/contract_to_booking_transaction.md)
- [Glossary: Contract Key](../glossary/contract_key.md)
