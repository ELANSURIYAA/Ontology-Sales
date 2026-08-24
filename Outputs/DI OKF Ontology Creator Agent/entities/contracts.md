---
title: Contracts
type: entity
description: Commercial agreements and service coverage terms with contract type, duration, and renewal attributes
resource: entities
tags: [contracts, dimension, agreements]
timestamp: 2026-07-28T00:00:00Z
---

# Contracts

## Business Definition

Describes the commercial agreement or service coverage terms associated with a booking, including contract type, duration, renewal behavior, and support coverage level.

Contracts define the commercial terms, service entitlements, and renewal conditions for booking transactions.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_contract

**Source Columns**: contract_key, contract_type, term_months, auto_renew_flag, coverage_level

---

## Attributes

- **contract_key** - Surrogate key that uniquely identifies a contract record in the contract dimension
- **contract_type** - Type of commercial agreement or support entitlement, such as Enterprise Agreement, SaaS Subscription, or Solution Support
- **term_months** - Number of months covered by the contract or subscription term
- **auto_renew_flag** - Indicator showing whether the contract is set to renew automatically at the end of its term
- **coverage_level** - Service or support coverage level provided under the contract

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

All booking-related measures can be analyzed by contract attributes:
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

- Each contract must have a unique contract_key
- contract_type defines the commercial model and entitlements
- term_months determines the contract duration and impacts ACV/TCV calculations
- auto_renew_flag indicates whether contracts renew automatically
- coverage_level defines the service and support entitlements
- Contract attributes enable renewal forecasting and contract value analysis

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
