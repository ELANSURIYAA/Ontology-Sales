---
title: Sales Representative
type: entity
description: Business entity representing sales personnel responsible for booking transactions.
resource: entities
tags: [entity, sales-representative, sales, workforce]
timestamp: 2026-07-28
---

# Sales Representative

## Business Definition
Stores information about sales personnel responsible for managing customer relationships and booking transactions.

## Technical Mapping
- Source Table: `QuoteToBooking.dim_sales_rep`
- Related Glossary: [Sales Representative](../glossary/sales-representative.md)

## Attributes
- Sales Representative Key
- Sales Representative ID
- Sales Representative Name
- Sales Role
- Sales Team
- Covered Segment

## Primary Keys
- Sales Representative Key

## Foreign Keys
None

## Measures
None

## Relationships
- [Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)

## Related Concepts
- [Sales Representative ID](../glossary/sales-representative-id.md)
- [Sales Representative Name](../glossary/sales-representative-name.md)
- [Sales Role](../glossary/sales-role.md)
- [Sales Team](../glossary/sales-team.md)
- [Covered Segment](../glossary/covered-segment.md)
- [Booking Transaction](booking-transaction.md)
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

## Business Rules
- Each sales representative record is uniquely identified by Sales Representative Key.
- A sales representative may be associated with multiple booking transactions.
- Covered Segment describes the customer segment for which the representative is responsible.
