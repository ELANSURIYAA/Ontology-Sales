---
title: Sales Representative to Booking Relationship
type: relationship
description: Foreign key relationship linking sales representative attributes to booking transactions
resource: relationships
tags: [okf, relationship, sales-rep, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative to Booking Relationship

## Business Description

This relationship links sales representative and organizational attributes to individual booking transactions, enabling analysis of bookings by sales person, role, team, and market segment coverage. Each booking transaction references a specific sales representative through the sales representative foreign key.

---

## Technical Mapping

**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Sales Representative Dimension](../entities/sales-representative-dimension.md)  
**Attribute**: sales_rep_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Fact](../entities/booking-fact.md)  
**Attribute**: sales_rep_key  
**Role**: Child (Many side)

---

## Relationship Semantics

- One sales representative can have many booking transactions
- Each booking transaction must reference exactly one sales representative
- The relationship enables sales performance analysis by representative
- Sales representative attributes provide context for understanding sales productivity and effectiveness

---

## Business Rules

1. Every booking must reference a valid sales representative record
2. Sales representative key in Booking Fact must exist in Sales Representative Dimension
3. Sales representative attributes remain consistent for a given sales representative key
4. Referential integrity must be maintained between dimensions and fact

---

## Analytical Use Cases

- Analyze sales performance by sales representative
- Track revenue by sales role and team
- Monitor quota attainment and productivity
- Evaluate segment coverage effectiveness
- Support sales capacity planning
- Measure sales representative contribution

---

## Related Concepts

### Related Domains
- [Sales Organization](../domains/sales-organization.md)
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
