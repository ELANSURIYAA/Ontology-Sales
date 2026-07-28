---
title: Geography
type: entity
description: Business entity representing reporting geography for sales performance analysis.
resource: entities
tags: [entity, geography, region, sales]
timestamp: 2026-07-28
---

# Geography

## Business Definition
Stores geographic attributes used to analyze bookings by sales region, theater, and country.

## Technical Mapping
- Source Table: `QuoteToBooking.dim_geography`
- Related Glossary: [Geography](../glossary/geography.md)

## Attributes
- Geography Key
- Sales Region
- Sales Theater
- Country

## Primary Keys
- Geography Key

## Foreign Keys
None

## Measures
None

## Relationships
- [Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)

## Related Concepts
- [Sales Region](../glossary/sales-region.md)
- [Sales Theater](../glossary/sales-theater.md)
- [Country](../glossary/country.md)
- [Booking Transaction](booking-transaction.md)
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

## Business Rules
- Each geography record is uniquely identified by Geography Key.
- Geography supports reporting by region, theater, and country.
- A geography may be associated with multiple booking transactions.
