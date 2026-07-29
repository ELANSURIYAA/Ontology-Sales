---
title: Geography to Booking Transaction
type: relationship
description: One-to-Many relationship linking geographies to booking transactions
resource: relationships
tags: [relationship, geography, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Geography to Booking Transaction

## Business Description

This relationship links Geography dimension records to Booking Transaction fact records. Each geography can be associated with multiple booking transactions, while each booking transaction occurs in exactly one geographic location. This relationship enables regional analysis of booking performance across sales regions, theaters, and countries.

---

## Relationship Details

**Relationship ID**: REL004  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Geography](../entities/geography.md)  
**Entity ID**: ENT004  
**Attribute**: Geography Key  
**Technical Column**: geography_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Entity ID**: ENT008  
**Attribute**: Geography Key  
**Technical Column**: geography_key  
**Role**: Child (Many side)

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_geography  
**Target Table**: QuoteToBooking.fact_bookings  
**Join Condition**: `dim_geography.geography_key = fact_bookings.geography_key`

---

## Business Rules

1. Each booking transaction must reference a valid geography
2. A geography can have zero or many booking transactions
3. Geography Key in Booking Transaction must exist in Geography dimension
4. Referential integrity must be maintained
5. Geographic attributes apply to all associated booking transactions

---

## Analytical Usage

This relationship enables analysis of:

- Booking performance by sales region
- Theater-level revenue contribution and trends
- Country-specific booking patterns
- Geographic market penetration and growth
- Regional quota attainment and performance

---

## Related Concepts

- [Geography](../entities/geography.md) - Source dimension entity
- [Booking Transaction](../entities/booking-transaction.md) - Target fact entity
- [Customer](../entities/customer.md) - Customer headquarters locations
- [Sales Representative](../entities/sales-representative.md) - Territory assignments
- [Partner](../entities/partner.md) - Partner geographic coverage

---

## Semantic Links

- [Relationship Index](./index.md)
- [Entity Index](../entities/index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Main Index](../index.md)

---

## Metadata

**Relationship ID**: REL004  
**Source Entity ID**: ENT004  
**Target Entity ID**: ENT008  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
