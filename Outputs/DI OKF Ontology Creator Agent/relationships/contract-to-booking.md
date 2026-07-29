---
title: Contract to Booking Relationship
type: relationship
description: Foreign key relationship linking contract attributes to booking transactions
resource: relationships
tags: [okf, relationship, contract, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Contract to Booking Relationship

## Business Description

This relationship links contract and service agreement attributes to individual booking transactions, enabling analysis of bookings by contract type, term, renewal behavior, and coverage level. Each booking transaction references a specific contract configuration through the contract foreign key.

---

## Technical Mapping

**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Contract Dimension](../entities/contract-dimension.md)  
**Attribute**: contract_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Fact](../entities/booking-fact.md)  
**Attribute**: contract_key  
**Role**: Child (Many side)

---

## Relationship Semantics

- One contract configuration can be associated with many booking transactions
- Each booking transaction must reference exactly one contract configuration
- The relationship enables analysis of booking performance by contract attributes
- Contract attributes provide context for understanding booking terms and conditions

---

## Business Rules

1. Every booking must reference a valid contract record
2. Contract key in Booking Fact must exist in Contract Dimension
3. Contract attributes remain consistent for a given contract key
4. Referential integrity must be maintained between dimensions and fact

---

## Analytical Use Cases

- Analyze bookings by contract type
- Track revenue by contract term
- Monitor auto-renewal rates
- Evaluate coverage level distribution
- Support renewal forecasting
- Measure contract performance

---

## Related Concepts

### Related Domains
- [Contract Management](../domains/contract-management.md)
- [Sales Transactions](../domains/sales-transactions.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Navigation

- [Back to Relationships Index](index.md)
- [Back to Bundle Index](../index.md)
