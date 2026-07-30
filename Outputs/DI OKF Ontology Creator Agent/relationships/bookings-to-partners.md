---
title: Bookings to Partners
type: relationship
description: Links booking transactions to the partner involved in fulfilling the sale
resource: relationships
tags: [bookings, partners, relationship, many-to-one]
timestamp: 2024-01-15T00:00:00Z
---

# Bookings to Partners

## Business Definition

This relationship links booking transactions to the partner involved in fulfilling the sale, enabling analysis of bookings by partner type, partner tier, and route to market.

---

## Relationship Details

**Source Entity**: [Booking Transaction](../entities/bookings.md)  
**Target Entity**: [Partner](../entities/partners.md)  
**Relationship Type**: Many-to-One  
**Cardinality**: Many bookings can be associated with one partner

---

## Technical Mapping

**Join Type**: Inner Join  
**Left Key**: bookings.partner_key  
**Right Key**: partners.partner_key

---

## Business Description

Each booking transaction is associated with a specific partner organization involved in fulfilling the sale. Partner attributes include partner type (distributor, reseller, systems integrator, direct channel), partner tier (program status level), and route to market (sales channel path). Multiple booking transactions can be associated with the same partner.

---

## Usage

This relationship enables analysis such as:

- Channel partner performance
- Partner type effectiveness
- Partner tier contribution
- Route to market analysis
- Direct vs indirect sales mix

---

## Related Concepts

- [Partner Type](../glossary/partner-type.md)
- [Partner Tier](../glossary/partner-tier.md)
- [Route to Market](../glossary/route-to-market.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Partner Entity](../entities/partners.md)
- [View Partners Domain](../domains/partners.md)
