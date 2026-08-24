---
title: Bookings to Contracts
type: relationship
description: Links booking transactions to contract terms and service coverage
resource: relationships
tags: [bookings, contracts, relationship, many-to-one]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Contracts

## Business Definition

Links booking transactions to the commercial agreement or service coverage terms associated with the booking, including contract type, duration, renewal behavior, and support coverage level.

This relationship enables analysis of booking performance by contract characteristics and supports contract value and renewal forecasting.

---

## Relationship Type

**many-to-one**

Multiple booking transactions can be associated with the same contract terms.

---

## Source Entity

[Bookings](../entities/bookings.md)

---

## Target Entity

[Contracts](../entities/contracts.md)

---

## Cardinality

- Each booking transaction must be associated with exactly one contract record
- Each contract record can be associated with multiple booking transactions

---

## Technical Mapping

**Join Condition**: bookings.contract_key = contracts.contract_key

**Left Dataset**: bookings (quotetobooking.fact_bookings)

**Right Dataset**: contracts (quotetobooking.dim_contract)

**Join Keys**:
- Left: contract_key
- Right: contract_key

---

## Business Purpose

This relationship enables:
- Analysis of bookings by contract type (Enterprise Agreement, SaaS Subscription, Solution Support)
- Contract term analysis and duration-based segmentation
- Renewal forecasting based on auto-renew flags
- Service coverage level analysis
- ACV and TCV calculations based on contract terms

---

## Related Measures

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)

---

## Related Concepts

- [Annual Contract Value](../glossary/annual-contract-value.md)
- [Total Contract Value](../glossary/total-contract-value.md)
- [Renewal](../glossary/renewal.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
