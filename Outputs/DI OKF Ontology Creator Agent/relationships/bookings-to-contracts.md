---
title: Bookings to Contracts
type: relationship
description: Links booking transactions to contract terms and conditions
resource: relationships
tags: [bookings, contracts, many-to-one, relationship]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Contracts

## Business Definition

The Bookings to Contracts relationship links individual booking transactions to their associated contract terms and conditions. This relationship enables analysis of booking performance by contract type, term duration, renewal behavior, and coverage level. It supports contract management, renewal forecasting, and revenue model analysis.

---

## Relationship Type

**Many-to-one**

Multiple booking transactions can be associated with the same contract record.

---

## Source Entity

**[Bookings](../entities/bookings.md)**

The fact table containing individual completed sales booking transactions.

---

## Target Entity

**[Contracts](../entities/contracts.md)**

The dimension table describing commercial agreements and service coverage terms.

---

## Cardinality

**Many Bookings : One Contract**

- Each booking transaction references exactly one contract record
- Multiple booking transactions can share the same contract
- Contract records can exist without associated bookings

---

## Join Specification

### Left Join Key
- **Field**: contract_key
- **Entity**: Bookings
- **Type**: Foreign Key

### Right Join Key
- **Field**: contract_key
- **Entity**: Contracts
- **Type**: Primary Key

### Join Condition
```sql
bookings.contract_key = contracts.contract_key
```

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings

**Target Table**: quotetobooking.dim_contract

**Join Column**: contract_key

---

## Business Purpose

This relationship enables:

- **Contract Type Analysis**: Analyze booking performance by contract type (Enterprise Agreement, SaaS Subscription, Solution Support)
- **Term Duration Analysis**: Track booking patterns by contract term length
- **Renewal Forecasting**: Identify contracts with auto-renewal for revenue forecasting
- **Coverage Level Analysis**: Analyze booking distribution by service coverage level
- **Revenue Model Tracking**: Monitor subscription vs perpetual license revenue
- **Contract Performance**: Evaluate contract effectiveness and customer preferences

---

## Related Measures

All booking measures can be analyzed by contract attributes:
- [Booking Count](../measures/booking-count.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)

---

## Related Concepts

- [Annual Contract Value](../glossary/annual-contract-value.md)
- [Total Contract Value](../glossary/total-contract-value.md)
- [Renewal](../glossary/renewal.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

1. **Mandatory Relationship**: Every booking must reference a valid contract
2. **Referential Integrity**: contract_key in bookings must exist in contracts dimension
3. **One Contract per Booking**: Each booking references exactly one contract record
4. **Contract Independence**: Contracts can exist without bookings (pre-defined contract templates)

---

## Usage Examples

### Contract Type Analysis
```sql
SELECT 
    contracts.contract_type,
    COUNT(bookings.booking_id) as booking_count,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN contracts ON bookings.contract_key = contracts.contract_key
GROUP BY contracts.contract_type
```

### Auto-Renewal Analysis
```sql
SELECT 
    contracts.auto_renew_flag,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN contracts ON bookings.contract_key = contracts.contract_key
GROUP BY contracts.auto_renew_flag
```

---

## Data Quality Rules

- contract_key in bookings must not be null
- contract_key in bookings must reference valid contract_key in contracts
- No orphaned bookings without contract references
- Contract dimension must be populated before booking transactions

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
