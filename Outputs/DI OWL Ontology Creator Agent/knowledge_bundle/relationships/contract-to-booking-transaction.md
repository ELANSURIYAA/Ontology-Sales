---
title: Contract to Booking Transaction
type: relationship
description: One-to-Many relationship linking contracts to booking transactions
resource: relationships
tags: [relationship, foreign-key, contract, booking-transaction]
timestamp: 2026-07-28T00:00:00Z
---

# Contract to Booking Transaction

## Business Description

This relationship links contract records to booking transactions, enabling analysis of bookings by contract attributes such as contract type, term, renewal behavior, and coverage level.

---

## Relationship Details

**Source Entity**: [Contract](../entities/contract.md)

**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Relationship Type**: Foreign Key

**Cardinality**: One-to-Many

**Confidence Score**: 1.00

---

## Technical Mapping

**Parent Table**: QuoteToBooking.dim_contract

**Parent Column**: contract_key

**Child Table**: QuoteToBooking.fact_bookings

**Child Column**: contract_key

---

## Cardinality Explanation

- **One Contract** can be associated with **Many Booking Transactions**
- **Each Booking Transaction** must reference **exactly one Contract**

This relationship enables:
- Analysis of booking amounts by contract type
- Evaluation of contract term preferences
- Measurement of renewal behavior
- Analysis of coverage level adoption

---

## Business Rules

1. Every booking transaction must reference a valid contract
2. A contract can be associated with zero or many booking transactions
3. Contract Key is the foreign key in the booking transaction fact table
4. The relationship is mandatory on the booking transaction side
5. The relationship supports referential integrity

---

## Related Concepts

- [Contract](../glossary/contract.md)
- [Contract Key](../glossary/contract-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Contract Type](../glossary/contract-type.md)
- [Contract Term Months](../glossary/contract-term-months.md)

---

## Usage Examples

**Analyze bookings by contract type**:
- Compare SaaS subscription vs. Enterprise Agreement bookings
- Measure contract type distribution

**Analyze bookings by contract term**:
- Evaluate average contract duration
- Compare short-term vs. long-term contract performance

**Analyze renewal behavior**:
- Measure auto-renewal adoption rates
- Compare renewal vs. new sale bookings

**Analyze coverage levels**:
- Evaluate premium vs. standard coverage bookings
- Measure support tier adoption

---

## Navigation

- [Back to Relationships Index](index.md)
- [View Source Entity: Contract](../entities/contract.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
