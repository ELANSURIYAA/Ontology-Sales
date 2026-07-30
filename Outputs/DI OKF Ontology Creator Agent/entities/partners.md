---
title: Partner
type: entity
description: Direct and indirect sales partners involved in fulfilling customer bookings, including partner identity, type, tier, and route to market
resource: entities
tags: [partner, channel, distribution, reseller, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Partner

## Business Definition

The Partner entity stores information about direct and indirect sales partners involved in fulfilling customer bookings, including partner identity, type, tier, and route to market. This entity enables channel performance analysis and partner ecosystem management.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_partner  
**Source Schema**: quotetobooking  
**Entity Type**: Dimension  
**Grain**: One row per partner

---

## Attributes

- partner_key
- partner_id
- partner_name
- partner_type
- partner_tier
- route_to_market

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

All booking and revenue measures can be analyzed by partner attributes:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

---

## Related Concepts

- [Partner Type](../glossary/partner-type.md)
- [Partner Tier](../glossary/partner-tier.md)
- [Route to Market](../glossary/route-to-market.md)

---

## Business Rules

### Partner Identification
Each partner is uniquely identified by partner_key (surrogate key) and partner_id (business key).

### Partner Type Classification
Partners are classified by type such as distributor, reseller, systems integrator, or direct channel.

### Partner Tier Assignment
Partner tier represents the program tier or status level assigned based on performance and capabilities.

### Route to Market
Route to market represents the sales channel path through which products or services are sold to customers.

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Partners Domain](../domains/partners.md)
