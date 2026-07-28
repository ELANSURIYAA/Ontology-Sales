---
title: Contract
type: entity
description: Business entity representing commercial agreement attributes associated with bookings.
resource: entities
tags: [entity, contract, sales, bookings]
timestamp: 2026-07-28
---

# Contract

## Business Definition
Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level.

## Technical Mapping
- Source Table: `QuoteToBooking.dim_contract`
- Related Glossary: [Contract](../glossary/contract.md)

## Attributes
- Contract Key
- Contract Type
- Contract Term Months
- Auto Renew Flag
- Coverage Level

## Primary Keys
- Contract Key

## Foreign Keys
None

## Measures
None

## Relationships
- [Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)

## Related Concepts
- [Contract Key](../glossary/contract-key.md)
- [Contract Type](../glossary/contract-type.md)
- [Contract Term Months](../glossary/contract-term-months.md)
- [Auto Renew Flag](../glossary/auto-renew-flag.md)
- [Coverage Level](../glossary/coverage-level.md)
- [Booking Transaction](booking-transaction.md)
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

## Business Rules
- Each contract record is uniquely identified by Contract Key.
- Contract records may be associated with multiple booking transactions.
