---
title: Contract to Booking Transaction
type: relationship
description: One-to-Many relationship linking contracts to booking transactions
resource: relationships
tags: [relationship, contract, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Contract to Booking Transaction

## Business Description

This relationship links Contract dimension records to Booking Transaction fact records. Each contract can be associated with multiple booking transactions, while each booking transaction references exactly one contract. This relationship enables analysis of booking performance by contract characteristics including contract type, term, renewal behavior, and coverage level.

---

## Relationship Details

**Relationship ID**: REL001  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Contract](../entities/contract.md)  
**Entity ID**: ENT001  
**Attribute**: Contract Key  
**Technical Column**: contract_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Entity ID**: ENT008  
**Attribute**: Contract Key  
**Technical Column**: contract_key  
**Role**: Child (Many side)

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract  
**Target Table**: QuoteToBooking.fact_bookings  
**Join Condition**: `dim_contract.contract_key = fact_bookings.contract_key`

---

## Business Rules

1. Each booking transaction must reference a valid contract
2. A contract can have zero or many booking transactions
3. Contract Key in Booking Transaction must exist in Contract dimension
4. Referential integrity must be maintained
5. Contract attributes apply to all associated booking transactions

---

## Analytical Usage

This relationship enables analysis of:

- Booking performance by contract type
- Revenue distribution by contract term
- Auto-renewal vs manual renewal patterns
- Coverage level adoption and performance
- Contract-based customer segmentation

---

## Related Concepts

- [Contract](../entities/contract.md) - Source dimension entity
- [Booking Transaction](../entities/booking-transaction.md) - Target fact entity
- [Customer](../entities/customer.md) - Customers with contracts
- [Product](../entities/product.md) - Products covered by contracts

---

## Semantic Links

- [Relationship Index](./index.md)
- [Entity Index](../entities/index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Main Index](../index.md)

---

## Metadata

**Relationship ID**: REL001  
**Source Entity ID**: ENT001  
**Target Entity ID**: ENT008  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
