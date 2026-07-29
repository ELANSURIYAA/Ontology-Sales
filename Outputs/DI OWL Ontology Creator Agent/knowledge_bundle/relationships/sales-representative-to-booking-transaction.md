---
title: Sales Representative to Booking Transaction
type: relationship
description: Foreign key relationship linking sales representatives to booking transactions
resource: relationships
tags: [sales, representative, booking, foreign-key, one-to-many]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative to Booking Transaction

## Relationship Definition

Links sales representative records to booking transactions, enabling analysis of bookings by sales role, sales team, and covered segment. This relationship allows business users to track sales representative performance and productivity.

---

## Relationship Identifier

**Relationship ID:** REL007

---

## Source Entity

**[Sales Representative](../entities/sales-representative.md)**  
**Entity ID:** ENT007  
**Technical Table:** QuoteToBooking.dim_sales_rep

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

**Parent Attribute:** Sales Representative Key (sales_rep_key)  
**Child Attribute:** Sales Representative Key (sales_rep_key)  
**Join Condition:** dim_sales_rep.sales_rep_key = fact_bookings.sales_rep_key

---

## Business Description

Each sales representative can be associated with multiple booking transactions, but each booking transaction is managed by exactly one sales representative. This relationship enables analysis of:

- Booking performance by sales representative
- Revenue contribution by sales role
- Sales team productivity analysis
- Covered segment performance
- Individual sales quota attainment

---

## Related Measures

This relationship enables sales representative-based analysis of:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)

---

## Business Use Cases

1. **Sales Representative Performance** - Track individual booking performance and quota attainment
2. **Sales Role Analysis** - Compare booking performance across different sales roles
3. **Sales Team Analysis** - Evaluate team-level productivity and revenue contribution
4. **Segment Coverage** - Analyze booking performance by covered customer segment
5. **Compensation Analysis** - Support sales commission and incentive calculations

---

## Navigation

- [Return to Relationships Index](./index.md)
- [View Source Entity: Sales Representative](../entities/sales-representative.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
