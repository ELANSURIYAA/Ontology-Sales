---
title: Partner
type: entity
description: Business entity describing channel and direct partners involved in the sales process.
resource: entities
tags: partner,entity,channel,sales
timestamp: 2026-07-28T00:00:00Z
---

# Partner

## Business Definition

Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market.

---

## Technical Mapping

- Source Table: `QuoteToBooking.dim_partner`
- Domain: [Sales Bookings and Revenue Analytics](../domains/sales_bookings_and_revenue_analytics.md)

---

## Attributes

- Partner Key (`partner_key`) - integer - not nullable
- Partner ID (`partner_id`) - character varying(20) - not nullable
- Partner Name (`partner_name`) - character varying(60)
- Partner Type (`partner_type`) - character varying(30)
- Partner Tier (`partner_tier`) - character varying(30)
- Route to Market (`route_to_market`) - character varying(20)

---

## Primary Keys

- Partner Key

---

## Foreign Keys

None

---

## Measures

None

---

## Relationships

- [Partner to Booking Transaction](../relationships/partner_to_booking_transaction.md)

---

## Related Concepts

- [Partner](../glossary/partner.md)
- [Partner ID](../glossary/partner_id.md)
- [Partner Name](../glossary/partner_name.md)
- [Partner Type](../glossary/partner_type.md)
- [Partner Tier](../glossary/partner_tier.md)
- [Route to Market](../glossary/route_to_market.md)

---

## Business Rules

- Each partner record is uniquely identified by Partner Key.
- Partner ID is the business identifier assigned to the partner organization.
- A partner can be associated with multiple booking transactions.

---

## Semantic Cross Links

- [Entities Index](index.md)
- [Domain](../domains/sales_bookings_and_revenue_analytics.md)
- [Booking Transaction](booking_transaction.md)
- [Partner to Booking Transaction](../relationships/partner_to_booking_transaction.md)
- [Glossary: Partner](../glossary/partner.md)
