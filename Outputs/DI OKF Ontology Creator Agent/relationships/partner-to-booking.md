---
title: Partner to Booking Relationship
type: relationship
description: Foreign key relationship linking partner attributes to booking transactions
resource: relationships
tags: [okf, relationship, partner, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Partner to Booking Relationship

## Business Description

This relationship links channel partner attributes to individual booking transactions, enabling analysis of bookings by partner identity, partner type, partner tier, and route to market. Each booking transaction references a specific partner through the partner foreign key.

---

## Technical Mapping

**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Partner Dimension](../entities/partner-dimension.md)  
**Attribute**: partner_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Fact](../entities/booking-fact.md)  
**Attribute**: partner_key  
**Role**: Child (Many side)

---

## Relationship Semantics

- One partner can have many booking transactions
- Each booking transaction must reference exactly one partner
- The relationship enables channel analysis of booking performance
- Partner attributes provide context for understanding channel sales patterns

---

## Business Rules

1. Every booking must reference a valid partner record
2. Partner key in Booking Fact must exist in Partner Dimension
3. Partner attributes remain consistent for a given partner key
4. Referential integrity must be maintained between dimensions and fact

---

## Analytical Use Cases

- Analyze sales performance by channel partner
- Track revenue by partner type and tier
- Evaluate route to market effectiveness
- Monitor partner program performance
- Identify top performing partners
- Support partner relationship management

---

## Related Concepts

### Related Domains
- [Partner Management](../domains/partner-management.md)
- [Sales Transactions](../domains/sales-transactions.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)

---

## Navigation

- [Back to Relationships Index](index.md)
- [Back to Bundle Index](../index.md)
