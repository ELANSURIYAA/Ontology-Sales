---
title: Customer to Booking Transaction
type: relationship
description: One-to-Many relationship linking customers to booking transactions
resource: relationships
tags: [relationship, customer, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Customer to Booking Transaction

## Business Description

This relationship links Customer dimension records to Booking Transaction fact records. Each customer can have multiple booking transactions, while each booking transaction is associated with exactly one customer. This relationship enables analysis of booking performance by customer characteristics including segment, industry, account tier, and headquarters location.

---

## Relationship Details

**Relationship ID**: REL002  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Customer](../entities/customer.md)  
**Entity ID**: ENT002  
**Attribute**: Customer Key  
**Technical Column**: customer_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Entity ID**: ENT008  
**Attribute**: Customer Key  
**Technical Column**: customer_key  
**Role**: Child (Many side)

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer  
**Target Table**: QuoteToBooking.fact_bookings  
**Join Condition**: `dim_customer.customer_key = fact_bookings.customer_key`

---

## Business Rules

1. Each booking transaction must reference a valid customer
2. A customer can have zero or many booking transactions
3. Customer Key in Booking Transaction must exist in Customer dimension
4. Referential integrity must be maintained
5. Customer attributes apply to all associated booking transactions

---

## Analytical Usage

This relationship enables analysis of:

- Booking performance by customer segment
- Revenue distribution by industry vertical
- Account tier contribution and performance
- Customer lifetime value and repeat purchase patterns
- Geographic customer distribution and headquarters analysis

---

## Related Concepts

- [Customer](../entities/customer.md) - Source dimension entity
- [Booking Transaction](../entities/booking-transaction.md) - Target fact entity
- [Geography](../entities/geography.md) - Customer locations
- [Sales Representative](../entities/sales-representative.md) - Customer account managers
- [Product](../entities/product.md) - Products purchased by customers

---

## Semantic Links

- [Relationship Index](./index.md)
- [Entity Index](../entities/index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Main Index](../index.md)

---

## Metadata

**Relationship ID**: REL002  
**Source Entity ID**: ENT002  
**Target Entity ID**: ENT008  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
