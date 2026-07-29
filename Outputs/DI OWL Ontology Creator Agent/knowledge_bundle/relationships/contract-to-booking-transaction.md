---
title: Contract to Booking Transaction
type: relationship
description: Foreign key relationship linking contracts to booking transactions
resource: relationships
tags: [contract, booking, foreign-key, one-to-many]
timestamp: 2026-07-28T00:00:00Z
---

# Contract to Booking Transaction

## Relationship Definition

Links contract records to booking transactions, enabling analysis of bookings by contract type, term, renewal behavior, and coverage level. This relationship allows business users to understand how different contract structures impact sales performance.

---

## Relationship Identifier

**Relationship ID:** REL001

---

## Source Entity

**[Contract](../entities/contract.md)**  
**Entity ID:** ENT001  
**Technical Table:** QuoteToBooking.dim_contract

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

**Parent Attribute:** Contract Key (contract_key)  
**Child Attribute:** Contract Key (contract_key)  
**Join Condition:** dim_contract.contract_key = fact_bookings.contract_key

---

## Business Description

Each contract can be associated with multiple booking transactions, but each booking transaction is linked to exactly one contract. This relationship enables analysis of:

- Booking performance by contract type
- Revenue analysis by contract term length
- Renewal behavior patterns
- Coverage level impact on bookings
- Contract value realization

---

## Related Measures

This relationship enables contract-based analysis of:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)

---

## Business Use Cases

1. **Contract Type Analysis** - Compare booking performance across different contract types
2. **Term Length Analysis** - Analyze revenue patterns by contract duration
3. **Renewal Analysis** - Track renewal rates and renewal booking values
4. **Coverage Level Analysis** - Evaluate booking performance by support coverage level
5. **Contract Value Analysis** - Compare actual bookings against contract values

---

## Navigation

- [Return to Relationships Index](./index.md)
- [View Source Entity: Contract](../entities/contract.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
