---
title: Sales Representative to Booking Transaction
type: relationship
description: One-to-Many relationship linking sales representatives to booking transactions
resource: relationships
tags: [relationship, sales-representative, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative to Booking Transaction

## Business Description

This relationship links Sales Representative dimension records to Booking Transaction fact records. Each sales representative can be associated with multiple booking transactions, while each booking transaction is credited to exactly one sales representative. This relationship enables sales performance analysis across representatives, roles, teams, and covered segments.

---

## Relationship Details

**Relationship ID**: REL007  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Sales Representative](../entities/sales-representative.md)  
**Entity ID**: ENT007  
**Attribute**: Sales Representative Key  
**Technical Column**: sales_rep_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Entity ID**: ENT008  
**Attribute**: Sales Representative Key  
**Technical Column**: sales_rep_key  
**Role**: Child (Many side)

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_sales_rep  
**Target Table**: QuoteToBooking.fact_bookings  
**Join Condition**: `dim_sales_rep.sales_rep_key = fact_bookings.sales_rep_key`

---

## Business Rules

1. Each booking transaction must reference a valid sales representative
2. A sales representative can have zero or many booking transactions
3. Sales Representative Key in Booking Transaction must exist in Sales Representative dimension
4. Referential integrity must be maintained
5. Sales representative attributes apply to all associated booking transactions

---

## Analytical Usage

This relationship enables analysis of:

- Individual sales representative performance and quota attainment
- Sales role effectiveness and productivity
- Sales team contribution and performance
- Segment coverage and specialization
- Representative ranking and leaderboards

---

## Related Concepts

- [Sales Representative](../entities/sales-representative.md) - Source dimension entity
- [Booking Transaction](../entities/booking-transaction.md) - Target fact entity
- [Customer](../entities/customer.md) - Customers managed by sales representatives
- [Geography](../entities/geography.md) - Sales territories
- [Product](../entities/product.md) - Products sold by representatives

---

## Semantic Links

- [Relationship Index](./index.md)
- [Entity Index](../entities/index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Main Index](../index.md)

---

## Metadata

**Relationship ID**: REL007  
**Source Entity ID**: ENT007  
**Target Entity ID**: ENT008  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
