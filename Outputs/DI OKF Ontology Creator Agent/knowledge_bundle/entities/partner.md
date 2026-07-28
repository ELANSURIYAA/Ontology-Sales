---
title: Partner
type: entity
description: Business entity representing the channel or direct partner involved in the sales process.
resource: entities
tags: [entity, partner, channel, sales]
timestamp: 2026-07-28
---

# Partner

## Business Definition
Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market.

## Technical Mapping
- Source Table: `QuoteToBooking.dim_partner`
- Related Glossary: [Partner](../glossary/partner.md)

## Attributes
- Partner Key
- Partner ID
- Partner Name
- Partner Type
- Partner Tier
- Route to Market

## Primary Keys
- Partner Key

## Foreign Keys
None

## Measures
None

## Relationships
- [Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)

## Related Concepts
- [Partner ID](../glossary/partner-id.md)
- [Partner Name](../glossary/partner-name.md)
- [Partner Type](../glossary/partner-type.md)
- [Partner Tier](../glossary/partner-tier.md)
- [Route to Market](../glossary/route-to-market.md)
- [Booking Transaction](booking-transaction.md)
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

## Business Rules
- Each partner record is uniquely identified by Partner Key.
- Partner ID is the business identifier assigned to the partner organization.
- A partner may be associated with multiple booking transactions.
