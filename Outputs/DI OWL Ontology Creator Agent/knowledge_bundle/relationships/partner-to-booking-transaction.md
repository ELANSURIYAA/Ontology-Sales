---
title: Partner to Booking Transaction
type: relationship
description: One-to-Many relationship linking partners to booking transactions
resource: relationships
tags: [relationship, partner, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Partner to Booking Transaction

## Business Description

This relationship links Partner dimension records to Booking Transaction fact records. Each partner can be associated with multiple booking transactions, while each booking transaction involves exactly one partner. This relationship enables channel analysis of booking performance across partner types, tiers, and routes to market.

---

## Relationship Details

**Relationship ID**: REL005  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Partner](../entities/partner.md)  
**Entity ID**: ENT005  
**Attribute**: Partner Key  
**Technical Column**: partner_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Entity ID**: ENT008  
**Attribute**: Partner Key  
**Technical Column**: partner_key  
**Role**: Child (Many side)

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_partner  
**Target Table**: QuoteToBooking.fact_bookings  
**Join Condition**: `dim_partner.partner_key = fact_bookings.partner_key`

---

## Business Rules

1. Each booking transaction must reference a valid partner
2. A partner can have zero or many booking transactions
3. Partner Key in Booking Transaction must exist in Partner dimension
4. Referential integrity must be maintained
5. Partner attributes apply to all associated booking transactions

---

## Analytical Usage

This relationship enables analysis of:

- Channel performance by partner type (distributor, reseller, systems integrator)
- Partner tier contribution (Gold, Silver, Bronze)
- Route-to-market effectiveness (direct, one-tier, two-tier)
- Partner revenue contribution and growth
- Channel mix and partner specialization

---

## Related Concepts

- [Partner](../entities/partner.md) - Source dimension entity
- [Booking Transaction](../entities/booking-transaction.md) - Target fact entity
- [Customer](../entities/customer.md) - Customers served through partners
- [Product](../entities/product.md) - Products sold through channels
- [Geography](../entities/geography.md) - Partner geographic coverage

---

## Semantic Links

- [Relationship Index](./index.md)
- [Entity Index](../entities/index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Main Index](../index.md)

---

## Metadata

**Relationship ID**: REL005  
**Source Entity ID**: ENT005  
**Target Entity ID**: ENT008  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
