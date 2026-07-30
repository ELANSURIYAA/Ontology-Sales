---
title: Contracts Domain
type: domain
description: Commercial agreement or service coverage terms associated with bookings, including contract type, duration, renewal behavior, and support coverage level
resource: domains
tags: [contracts, agreements, terms, coverage, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Contracts Domain

## Business Definition

The Contracts domain describes the commercial agreement or service coverage terms associated with a booking, including contract type, duration, renewal behavior, and support coverage level. This domain enables contract portfolio analysis and renewal management.

---

## Business Purpose

The Contracts domain enables analysis of:

- Contract type mix and performance
- Contract term length analysis
- Auto-renewal behavior tracking
- Coverage level distribution
- Contract portfolio health
- Renewal opportunity identification

---

## Domain Type

**Dimension Domain** - Descriptive attributes for contract analysis

---

## Related Entities

- [Contract](../entities/contracts.md)

---

## Related Measures

All booking and revenue measures can be analyzed by contract attributes:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

---

## Related Relationships

- [Bookings to Contracts](../relationships/bookings-to-contracts.md)

---

## Key Concepts

### Contract Type
Type of commercial agreement or support entitlement, such as Enterprise Agreement, SaaS Subscription, or Solution Support.

### Term Months
Number of months covered by the contract or subscription term for duration analysis.

### Auto Renew Flag
Indicator showing whether the contract is set to renew automatically at the end of its term.

### Coverage Level
Service or support coverage level provided under the contract for entitlement management.

---

## Semantic Links

### Related Domains
- [Bookings Domain](bookings.md) - Contract-based bookings
- [Customers Domain](customers.md) - Contract holders

### Related Glossary
- [Contract Type](../glossary/contract-type.md)
- [Term Months](../glossary/term-months.md)
- [Auto Renew Flag](../glossary/auto-renew-flag.md)
- [Coverage Level](../glossary/coverage-level.md)

---

## Technical Mapping

**Source Table**: quotetobooking.dim_contract  
**Primary Key**: contract_key

---

## Navigation

- [Return to Domains Index](index.md)
- [Return to Main Index](../index.md)
- [View Contract Entity](../entities/contracts.md)
