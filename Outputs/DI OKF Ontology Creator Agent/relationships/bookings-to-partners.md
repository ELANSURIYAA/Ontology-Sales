---
title: Bookings to Partners
type: relationship
description: Links booking transactions to sales partners and channels
resource: relationships
tags: [bookings, partners, relationship, many-to-one]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Partners

## Business Definition

Links booking transactions to direct and indirect sales partners involved in fulfilling customer bookings, including partner identity, type, tier, and route to market.

This relationship enables analysis of partner channel performance and supports partner program effectiveness and channel strategy analysis.

---

## Relationship Type

**many-to-one**

Multiple booking transactions can be associated with the same partner.

---

## Source Entity

[Bookings](../entities/bookings.md)

---

## Target Entity

[Partners](../entities/partners.md)

---

## Cardinality

- Each booking transaction must be associated with exactly one partner record
- Each partner record can be associated with multiple booking transactions

---

## Technical Mapping

**Join Condition**: bookings.partner_key = partners.partner_key

**Left Dataset**: bookings (quotetobooking.fact_bookings)

**Right Dataset**: partners (quotetobooking.dim_partner)

**Join Keys**:
- Left: partner_key
- Right: partner_key

---

## Business Purpose

This relationship enables:
- Partner channel performance analysis
- Partner type analysis (distributor, reseller, systems integrator, direct)
- Partner tier and program effectiveness analysis
- Route to market strategy analysis
- Partner profitability and incentive analysis
- Channel mix optimization

---

## Related Measures

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Booking Count](../measures/booking-count.md)

---

## Related Concepts

- [Route to Market](../glossary/route-to-market.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
