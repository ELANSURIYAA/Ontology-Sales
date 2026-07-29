---
title: Partner to Booking Transaction
type: relationship
description: Foreign key relationship linking partners to booking transactions
resource: relationships
tags: [partner, booking, foreign-key, one-to-many, channel]
timestamp: 2026-07-28T00:00:00Z
---

# Partner to Booking Transaction

## Relationship Definition

Links partner records to booking transactions, enabling analysis of bookings by partner type, partner tier, and route to market. This relationship allows business users to understand channel partner effectiveness and contribution to revenue.

---

## Relationship Identifier

**Relationship ID:** REL005

---

## Source Entity

**[Partner](../entities/partner.md)**  
**Entity ID:** ENT005  
**Technical Table:** QuoteToBooking.dim_partner

---

## Target Entity

**[Booking Transaction](../entities/booking-transaction.md)**  
**Entity ID:** ENT008  
**Technical Table:** QuoteToBooking.fact_bookings

---

## Relationship Type

**Type:** Foreign Key  
**Cardinality:** One-to-Many  
**Confidence Score:** 1.00

---

## Technical Mapping

**Parent Attribute:** Partner Key (partner_key)  
**Child Attribute:** Partner Key (partner_key)  
**Join Condition:** dim_partner.partner_key = fact_bookings.partner_key

---

## Business Description

Each partner can be associated with multiple booking transactions, but each booking transaction is facilitated by exactly one partner. This relationship enables analysis of:

- Booking performance by partner type
- Revenue contribution by partner tier
- Route to market effectiveness
- Channel partner productivity
- Partner program performance

---

## Related Measures

This relationship enables partner-based analysis of:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)

---

## Business Use Cases

1. **Partner Type Analysis** - Compare booking performance across distributors, resellers, and direct sales
2. **Partner Tier Analysis** - Evaluate revenue contribution by partner certification tier
3. **Route to Market Analysis** - Analyze booking patterns by sales delivery path
4. **Partner Productivity** - Calculate bookings per partner and identify top performers
5. **Channel Strategy** - Optimize partner mix and channel investment

---

## Navigation

- [Return to Relationships Index](./index.md)
- [View Source Entity: Partner](../entities/partner.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
