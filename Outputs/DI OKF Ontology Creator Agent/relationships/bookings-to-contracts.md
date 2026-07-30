---
title: Bookings to Contracts
type: relationship
description: Links booking transactions to their associated contract terms and conditions
resource: relationships
tags: [bookings, contracts, relationship, many-to-one]
timestamp: 2024-01-15T00:00:00Z
---

# Bookings to Contracts

## Business Definition

This relationship links booking transactions to their associated contract terms and conditions, enabling analysis of bookings by contract type, term duration, renewal behavior, and coverage level.

---

## Relationship Details

**Source Entity**: [Booking Transaction](../entities/bookings.md)  
**Target Entity**: [Contract](../entities/contracts.md)  
**Relationship Type**: Many-to-One  
**Cardinality**: Many bookings can be associated with one contract

---

## Technical Mapping

**Join Type**: Inner Join  
**Left Key**: bookings.contract_key  
**Right Key**: contracts.contract_key

---

## Business Description

Each booking transaction is associated with a specific contract that defines the commercial agreement terms, including contract type (e.g., Enterprise Agreement, SaaS Subscription), term duration in months, auto-renewal behavior, and service coverage level. Multiple booking transactions can be associated with the same contract.

---

## Usage

This relationship enables analysis such as:

- Bookings by contract type
- Contract term length analysis
- Auto-renewal contract performance
- Coverage level distribution
- Contract portfolio health metrics

---

## Related Concepts

- [Contract Type](../glossary/contract-type.md)
- [Term Months](../glossary/term-months.md)
- [Auto Renew Flag](../glossary/auto-renew-flag.md)
- [Coverage Level](../glossary/coverage-level.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Contract Entity](../entities/contracts.md)
- [View Contracts Domain](../domains/contracts.md)
