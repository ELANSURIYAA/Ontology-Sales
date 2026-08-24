---
title: Partners
type: entity
description: Direct and indirect sales partners with type, tier, and route to market attributes
resource: entities
tags: [partners, dimension, channels]
timestamp: 2026-07-28T00:00:00Z
---

# Partners

## Business Definition

Stores information about direct and indirect sales partners involved in fulfilling customer bookings, including partner identity, type, tier, and route to market.

Partners represent the channel organizations, distributors, resellers, and systems integrators that facilitate sales transactions.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_partner

**Source Columns**: partner_key, partner_id, partner_name, partner_type, partner_tier, route_to_market

---

## Attributes

- **partner_key** - Surrogate key that uniquely identifies a partner record in the partner dimension
- **partner_id** - Business identifier assigned to the partner organization
- **partner_name** - Official name of the partner organization
- **partner_type** - Classification of the partner, such as distributor, reseller, systems integrator, or direct channel
- **partner_tier** - Program tier or status level assigned to the partner
- **route_to_market** - Sales channel path through which the product or service is sold to the customer

---

## Primary Keys

- partner_key

---

## Foreign Keys

None

---

## Relationships

- [Bookings to Partners](../relationships/bookings-to-partners.md)

---

## Measures

All booking-related measures can be analyzed by partner attributes:
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Booking Count](../measures/booking-count.md)

---

## Related Concepts

- [Route to Market](../glossary/route-to-market.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

- Each partner must have a unique partner_key
- partner_id serves as the natural business identifier
- Partners are classified by type (distributor, reseller, systems integrator, direct)
- partner_tier indicates program status and benefits level
- route_to_market defines the channel strategy for reaching customers
- Partner performance can be analyzed by type, tier, and route to market

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
