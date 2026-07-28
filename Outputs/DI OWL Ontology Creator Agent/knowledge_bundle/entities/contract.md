---
title: Contract
type: entity
description: Commercial agreements associated with bookings including contract type, term, renewal behavior, and support coverage level
resource: entities
tags: [entity, dimension, contract, agreement, commercial]
timestamp: 2026-07-28T00:00:00Z
---

# Contract

## Business Definition

Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract

**Source System**: QuoteToBooking

**Entity Type**: Dimension

---

## Attributes

- **Contract Key** (contract_key): Surrogate key that uniquely identifies a contract record in the contract dimension
- **Contract Type** (contract_type): Describes the type of commercial agreement attached to the booking, such as SaaS subscription, Enterprise Agreement, or support contract
- **Contract Term Months** (term_months): Indicates the duration of the contract in months
- **Auto Renew Flag** (auto_renew_flag): Indicates whether the contract is set to renew automatically at the end of its term
- **Coverage Level** (coverage_level): Describes the level of service or support coverage provided under the contract

---

## Primary Keys

- **Contract Key** (contract_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- **[Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)**: One-to-Many relationship linking contracts to booking transactions

### Related Entities

- [Booking Transaction](booking-transaction.md): Fact entity that references this dimension

---

## Measures

This dimension supports analysis of the following measures:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Concepts

- [Contract](../glossary/contract.md)
- [Contract Key](../glossary/contract-key.md)
- [Contract Type](../glossary/contract-type.md)
- [Contract Term Months](../glossary/contract-term-months.md)
- [Auto Renew Flag](../glossary/auto-renew-flag.md)
- [Coverage Level](../glossary/coverage-level.md)
- [Annual Contract Value USD](../glossary/annual-contract-value-usd.md)
- [Total Contract Value USD](../glossary/total-contract-value-usd.md)

---

## Business Rules

1. Contract Key is a surrogate key and must be unique
2. Contract Type classifies the commercial agreement (e.g., SaaS subscription, Enterprise Agreement, support contract)
3. Contract Term Months indicates the duration of the contract commitment
4. Auto Renew Flag indicates automatic renewal behavior
5. Coverage Level describes the service or support tier
6. Every booking transaction must reference a valid contract
7. Contract terms are measured in months
8. Annual Contract Value (ACV) is derived from the contract value annualized
9. Total Contract Value (TCV) represents the full contract commitment

---

## Usage Examples

**Analysis by Contract Type**:
- Compare booking amounts across SaaS subscriptions vs. Enterprise Agreements
- Analyze renewal rates by contract type

**Analysis by Contract Term**:
- Evaluate average contract duration by customer segment
- Compare TCV for short-term vs. long-term contracts

**Analysis by Coverage Level**:
- Measure booking amounts by support coverage tier
- Analyze premium vs. standard coverage adoption

**Analysis by Auto Renew Behavior**:
- Calculate percentage of contracts with auto-renewal enabled
- Compare retention rates for auto-renew vs. manual renewal contracts

---

## Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Main Index](../index.md)
- [View Relationships](../relationships/index.md)
- [View Measures](../measures/index.md)
- [View Glossary](../glossary/index.md)
