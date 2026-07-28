---
title: Sales Representative to Booking Transaction
type: relationship
description: Foreign key relationship linking sales personnel to booking transactions
resource: relationships
tags: [relationship, foreign-key, sales-rep, booking, one-to-many, sales-team]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative to Booking Transaction

## Business Definition

Links sales personnel to booking transactions, enabling analysis of individual and team sales performance by sales role, sales team, and covered segment to support sales organization effectiveness and performance management.

---

## Relationship Details

**Relationship ID**: REL007  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Sales Representative](../entities/sales-representative.md)  
**Attribute**: Sales Representative Key (sales_rep_key)  
**Role**: Parent/Dimension

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Sales Representative Key (sales_rep_key)  
**Role**: Child/Fact

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_sales_rep  
**Source Column**: sales_rep_key  
**Target Table**: QuoteToBooking.fact_bookings  
**Target Column**: sales_rep_key  
**Join Type**: INNER JOIN

---

## Business Description

Each booking transaction is associated with exactly one sales representative who managed the customer relationship and facilitated the booking. A single sales representative can have multiple booking transactions as they manage multiple customers and opportunities.

This relationship enables business users to:
- Analyze booking amounts by sales representative
- Compare sales team performance
- Evaluate sales role effectiveness
- Track individual quota attainment
- Assess sales productivity
- Monitor segment coverage effectiveness

---

## Relationship Rules

1. **Cardinality**: One sales representative can have many booking transactions (One-to-Many)
2. **Referential Integrity**: Every booking transaction must reference a valid sales representative record
3. **Mandatory**: Sales Representative Key is required in booking transactions for sales performance analysis
4. **Immutable**: Sales representative association should not change after booking is recorded

---

## Usage Examples

### Analyze Bookings by Sales Representative
```sql
SELECT s.rep_name, SUM(b.booking_amount_usd)
FROM dim_sales_rep s
JOIN fact_bookings b ON s.sales_rep_key = b.sales_rep_key
GROUP BY s.rep_name
ORDER BY SUM(b.booking_amount_usd) DESC
```

### Compare Sales Team Performance
```sql
SELECT s.sales_team, SUM(b.booking_amount_usd), COUNT(b.booking_id)
FROM dim_sales_rep s
JOIN fact_bookings b ON s.sales_rep_key = b.sales_rep_key
GROUP BY s.sales_team
```

---

## Related Concepts

### Related Entities
- [Sales Representative](../entities/sales-representative.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

### Related Glossary Terms
- [Sales Representative](../glossary/sales-representative.md)
- [Sales Representative Key](../glossary/sales-representative-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [View Relationships Index](index.md)
- [View Sales Representative Entity](../entities/sales-representative.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Relationship ID**: REL007  
**Source**: Sales Representative  
**Target**: Booking Transaction  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Last Updated**: 2026-07-28T00:00:00Z
