---
title: Geography to Booking Relationship
type: relationship
description: Foreign key relationship linking geographic attributes to booking transactions
resource: relationships
tags: [okf, relationship, geography, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Geography to Booking Relationship

## Business Description

This relationship links geographic attributes to individual booking transactions, enabling analysis of bookings by region, theater, and country. Each booking transaction references a specific geography through the geography foreign key.

---

## Technical Mapping

**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Geography Dimension](../entities/geography-dimension.md)  
**Attribute**: geography_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Fact](../entities/booking-fact.md)  
**Attribute**: geography_key  
**Role**: Child (Many side)

---

## Relationship Semantics

- One geography can have many booking transactions
- Each booking transaction must reference exactly one geography
- The relationship enables geographic analysis of booking performance
- Geography attributes provide context for understanding regional sales patterns

---

## Business Rules

1. Every booking must reference a valid geography record
2. Geography key in Booking Fact must exist in Geography Dimension
3. Geography attributes remain consistent for a given geography key
4. Referential integrity must be maintained between dimensions and fact

---

## Analytical Use Cases

- Analyze sales performance by geographic region
- Track revenue by theater and country
- Monitor regional growth trends
- Support territory planning and coverage
- Evaluate geographic market penetration
- Compare performance across geographies

---

## Related Concepts

### Related Domains
- [Geography](../domains/geography.md)
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
