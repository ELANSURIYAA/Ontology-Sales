---
title: Date to Booking Transaction
type: relationship
description: One-to-Many relationship linking dates to booking transactions
resource: relationships
tags: [relationship, date, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Date to Booking Transaction

## Business Description

This relationship links Date dimension records to Booking Transaction fact records. Each date can be associated with multiple booking transactions, while each booking transaction occurs on exactly one date. This relationship enables time-based analysis of booking performance across calendar and fiscal periods.

---

## Relationship Details

**Relationship ID**: REL003  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Date](../entities/date.md)  
**Entity ID**: ENT003  
**Attribute**: Date Key  
**Technical Column**: date_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Entity ID**: ENT008  
**Attribute**: Booking Date Key  
**Technical Column**: date_key  
**Role**: Child (Many side)

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_date  
**Target Table**: QuoteToBooking.fact_bookings  
**Join Condition**: `dim_date.date_key = fact_bookings.date_key`

---

## Business Rules

1. Each booking transaction must reference a valid date
2. A date can have zero or many booking transactions
3. Date Key in Booking Transaction must exist in Date dimension
4. Referential integrity must be maintained
5. Date attributes apply to all associated booking transactions

---

## Analytical Usage

This relationship enables analysis of:

- Booking trends over time (daily, monthly, quarterly, yearly)
- Calendar year vs fiscal year performance comparison
- Seasonal patterns and booking cycles
- Period-over-period growth analysis
- Fiscal quarter and year-end performance tracking

---

## Related Concepts

- [Date](../entities/date.md) - Source dimension entity
- [Booking Transaction](../entities/booking-transaction.md) - Target fact entity
- [Contract](../entities/contract.md) - Contract effective dates
- [Customer](../entities/customer.md) - Customer acquisition timing

---

## Semantic Links

- [Relationship Index](./index.md)
- [Entity Index](../entities/index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Main Index](../index.md)

---

## Metadata

**Relationship ID**: REL003  
**Source Entity ID**: ENT003  
**Target Entity ID**: ENT008  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
