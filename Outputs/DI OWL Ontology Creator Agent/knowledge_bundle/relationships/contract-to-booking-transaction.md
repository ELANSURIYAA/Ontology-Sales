---
title: Contract to Booking Transaction
type: relationship
description: Foreign key relationship linking contract agreements to booking transactions
resource: relationships
tags: [relationship, foreign-key, contract, booking, one-to-many]
timestamp: 2026-07-28T00:00:00Z
---

# Contract to Booking Transaction

## Business Definition

Links contract agreements to booking transactions, enabling analysis of booking performance by contract characteristics including contract type, term, renewal behavior, and coverage level.

---

## Relationship Details

**Relationship ID**: REL001  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Contract](../entities/contract.md)  
**Attribute**: Contract Key (contract_key)  
**Role**: Parent/Dimension

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Contract Key (contract_key)  
**Role**: Child/Fact

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract  
**Source Column**: contract_key  
**Target Table**: QuoteToBooking.fact_bookings  
**Target Column**: contract_key  
**Join Type**: INNER JOIN

---

## Business Description

Each booking transaction is associated with exactly one contract agreement that defines the commercial terms, duration, renewal behavior, and support coverage. A single contract can be referenced by multiple booking transactions over time as customers place orders under the same contractual agreement.

This relationship enables business users to:
- Analyze booking amounts by contract type
- Track renewal rates by contract characteristics
- Evaluate contract term effectiveness
- Assess auto-renewal adoption
- Compare performance across coverage levels

---

## Relationship Rules

1. **Cardinality**: One contract can have many booking transactions (One-to-Many)
2. **Referential Integrity**: Every booking transaction must reference a valid contract record
3. **Mandatory**: Contract Key is required in booking transactions for complete analysis
4. **Immutable**: Contract association should not change after booking is recorded

---

## Usage Examples

### Analyze Bookings by Contract Type
```sql
SELECT c.contract_type, SUM(b.booking_amount_usd)
FROM dim_contract c
JOIN fact_bookings b ON c.contract_key = b.contract_key
GROUP BY c.contract_type
```

### Evaluate Auto-Renewal Performance
```sql
SELECT c.auto_renew_flag, COUNT(b.booking_id), SUM(b.acv_usd)
FROM dim_contract c
JOIN fact_bookings b ON c.contract_key = b.contract_key
GROUP BY c.auto_renew_flag
```

---

## Related Concepts

### Related Entities
- [Contract](../entities/contract.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

### Related Glossary Terms
- [Contract](../glossary/contract.md)
- [Contract Key](../glossary/contract-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [View Relationships Index](index.md)
- [View Contract Entity](../entities/contract.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Relationship ID**: REL001  
**Source**: Contract  
**Target**: Booking Transaction  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Last Updated**: 2026-07-28T00:00:00Z
