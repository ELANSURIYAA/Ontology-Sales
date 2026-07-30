---
title: Contract
type: entity
description: Commercial agreement or service coverage terms associated with bookings, including contract type, duration, renewal behavior, and support coverage level
resource: entities
tags: [contract, agreement, terms, coverage, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Contract

## Business Definition

The Contract entity describes the commercial agreement or service coverage terms associated with a booking, including contract type, duration, renewal behavior, and support coverage level. This entity enables contract portfolio analysis and renewal management.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_contract  
**Source Schema**: quotetobooking  
**Entity Type**: Dimension  
**Grain**: One row per contract

---

## Attributes

- contract_key
- contract_type
- term_months
- auto_renew_flag
- coverage_level

---

## Primary Keys

- contract_key

---

## Foreign Keys

None

---

## Relationships

- [Bookings to Contracts](../relationships/bookings-to-contracts.md)

---

## Measures

All booking and revenue measures can be analyzed by contract attributes:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

---

## Related Concepts

- [Contract Type](../glossary/contract-type.md)
- [Term Months](../glossary/term-months.md)
- [Auto Renew Flag](../glossary/auto-renew-flag.md)
- [Coverage Level](../glossary/coverage-level.md)

---

## Business Rules

### Contract Type Classification
Contract types include Enterprise Agreement, SaaS Subscription, Solution Support, and other commercial agreements.

### Term Duration
Term months represents the number of months covered by the contract or subscription term.

### Auto Renewal Behavior
Auto renew flag indicates whether the contract is set to renew automatically at the end of its term.

### Coverage Level Assignment
Coverage level represents the service or support coverage level provided under the contract.

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Contracts Domain](../domains/contracts.md)
