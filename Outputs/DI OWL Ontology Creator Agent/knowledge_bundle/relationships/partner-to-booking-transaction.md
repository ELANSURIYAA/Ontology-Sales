---
title: Partner to Booking Transaction
type: relationship
description: One-to-Many relationship linking partners to booking transactions
resource: relationships
tags: [relationship, foreign-key, partner, booking-transaction, channel]
timestamp: 2026-07-28T00:00:00Z
---

# Partner to Booking Transaction

## Business Description

This relationship links partner records to booking transactions, enabling analysis of bookings by partner type, partner tier, and route to market.

---

## Relationship Details

**Source Entity**: [Partner](../entities/partner.md)

**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Relationship Type**: Foreign Key

**Cardinality**: One-to-Many

**Confidence Score**: 1.00

---

## Technical Mapping

**Parent Table**: QuoteToBooking.dim_partner

**Parent Column**: partner_key

**Child Table**: QuoteToBooking.fact_bookings

**Child Column**: partner_key

---

## Cardinality Explanation

- **One Partner** can be associated with **Many Booking Transactions**
- **Each Booking Transaction** must reference **exactly one Partner**

This relationship enables:
- Analysis of booking amounts by partner type
- Evaluation of partner tier performance
- Measurement of route to market effectiveness
- Channel performance analysis

---

## Business Rules

1. Every booking transaction must reference a valid partner
2. A partner can be associated with zero or many booking transactions
3. Partner Key is the foreign key in the booking transaction fact table
4. The relationship is mandatory on the booking transaction side
5. The relationship supports referential integrity

---

## Related Concepts

- [Partner](../glossary/partner.md)
- [Partner Key](../glossary/partner-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Partner Type](../glossary/partner-type.md)
- [Partner Tier](../glossary/partner-tier.md)
- [Route to Market](../glossary/route-to-market.md)

---

## Usage Examples

**Analyze bookings by partner type**:
- Compare distributor vs. reseller vs. systems integrator performance
- Measure direct vs. indirect sales

**Analyze bookings by partner tier**:
- Evaluate strategic vs. standard partner performance
- Measure partner tier effectiveness

**Analyze bookings by route to market**:
- Compare sales delivery paths
- Evaluate channel strategy effectiveness

**Partner performance analysis**:
- Identify top-performing partners
- Measure partner productivity
- Analyze partner product mix

---

## Navigation

- [Back to Relationships Index](index.md)
- [View Source Entity: Partner](../entities/partner.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
