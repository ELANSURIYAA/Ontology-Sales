---
title: Customer to Booking Relationship
type: relationship
description: Foreign key relationship linking customer attributes to booking transactions
resource: relationships
tags: [okf, relationship, customer, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Customer to Booking Relationship

## Business Description

This relationship links customer master data attributes to individual booking transactions, enabling analysis of bookings by customer identity, segment, industry, account tier, and headquarters location. Each booking transaction references a specific customer through the customer foreign key.

---

## Technical Mapping

**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Customer Dimension](../entities/customer-dimension.md)  
**Attribute**: customer_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Fact](../entities/booking-fact.md)  
**Attribute**: customer_key  
**Role**: Child (Many side)

---

## Relationship Semantics

- One customer can have many booking transactions
- Each booking transaction must reference exactly one customer
- The relationship enables customer-centric analysis of booking performance
- Customer attributes provide context for understanding booking patterns and customer behavior

---

## Business Rules

1. Every booking must reference a valid customer record
2. Customer key in Booking Fact must exist in Customer Dimension
3. Customer attributes remain consistent for a given customer key
4. Referential integrity must be maintained between dimensions and fact

---

## Analytical Use Cases

- Analyze bookings by customer segment
- Track revenue by industry vertical
- Evaluate account tier profitability
- Monitor customer lifetime value
- Identify top customers by revenue
- Support customer segmentation analysis

---

## Related Concepts

### Related Domains
- [Customer Management](../domains/customer-management.md)
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
