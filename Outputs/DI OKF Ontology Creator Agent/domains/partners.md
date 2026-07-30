---
title: Partners Domain
type: domain
description: Direct and indirect sales partners involved in fulfilling customer bookings, including partner identity, type, tier, and route to market
resource: domains
tags: [partners, channel, distribution, reseller, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Partners Domain

## Business Definition

The Partners domain stores information about direct and indirect sales partners involved in fulfilling customer bookings, including partner identity, type, tier, and route to market. This domain enables channel performance analysis and partner ecosystem management.

---

## Business Purpose

The Partners domain enables analysis of:

- Channel partner performance
- Partner type and tier effectiveness
- Route to market strategy
- Direct vs indirect sales mix
- Partner program success
- Channel revenue contribution

---

## Domain Type

**Dimension Domain** - Descriptive attributes for partner and channel analysis

---

## Related Entities

- [Partner](../entities/partners.md)

---

## Related Measures

All booking and revenue measures can be analyzed by partner attributes:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

---

## Related Relationships

- [Bookings to Partners](../relationships/bookings-to-partners.md)

---

## Key Concepts

### Partner Type
Classification of the partner such as distributor, reseller, systems integrator, or direct channel.

### Partner Tier
Program tier or status level assigned to the partner based on performance and capabilities.

### Route to Market
Sales channel path through which the product or service is sold to the customer.

---

## Semantic Links

### Related Domains
- [Bookings Domain](bookings.md) - Partner-facilitated sales
- [Customers Domain](customers.md) - Partner-served customers
- [Products Domain](products.md) - Partner-sold products

### Related Glossary
- [Partner Type](../glossary/partner-type.md)
- [Partner Tier](../glossary/partner-tier.md)
- [Route to Market](../glossary/route-to-market.md)

---

## Technical Mapping

**Source Table**: quotetobooking.dim_partner  
**Primary Key**: partner_key  
**Business Key**: partner_id

---

## Navigation

- [Return to Domains Index](index.md)
- [Return to Main Index](../index.md)
- [View Partner Entity](../entities/partners.md)
