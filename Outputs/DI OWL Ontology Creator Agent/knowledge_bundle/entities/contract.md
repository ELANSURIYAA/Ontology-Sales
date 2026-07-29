---
title: Contract
type: entity
description: Commercial agreements associated with bookings including contract type, term, renewal behavior, and support coverage level
resource: entities
tags: [contract, agreement, commercial, dimension]
timestamp: 2026-07-28T00:00:00Z
---

# Contract

## Business Definition

Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level. Contracts define the terms and conditions under which products and services are sold to customers.

---

## Entity Identifier

**Entity ID:** ENT001  
**Domain:** [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_contract  
**Table Type:** Dimension Table

---

## Attributes

- **Contract Key** - Surrogate key that uniquely identifies a contract record in the contract dimension
- **Contract Type** - Describes the type of commercial agreement attached to the booking, such as SaaS subscription, Enterprise Agreement, or support contract
- **Contract Term Months** - Indicates the duration of the contract in months
- **Auto Renew Flag** - Indicates whether the contract is set to renew automatically at the end of its term
- **Coverage Level** - Describes the level of service or support coverage provided under the contract

---

## Primary Keys

- **Contract Key** (contract_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- **[Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)** - One-to-Many relationship linking contracts to booking transactions

---

## Measures

Contracts are analyzed using measures from related [Booking Transaction](./booking-transaction.md) entity:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Business Rules

1. Each contract must have a unique Contract Key
2. Contract Term Months indicates the commitment period for the agreement
3. Auto Renew Flag determines whether the contract continues automatically
4. Coverage Level defines the service tier provided to the customer
5. Contract Type categorizes the commercial agreement structure

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Transactions associated with this contract
- [Customer](./customer.md) - Customers who enter into contracts
- [Product](./product.md) - Products covered by contracts
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md) - Value metric for contract analysis
- [Total Contract Value USD](../measures/total-contract-value-usd.md) - Total value metric for contract analysis

---

## Glossary Terms

- [Contract](../glossary/contract.md)
- [Contract Key](../glossary/contract-key.md)
- [Contract Type](../glossary/contract-type.md)
- [Contract Term Months](../glossary/contract-term-months.md)
- [Auto Renew Flag](../glossary/auto-renew-flag.md)
- [Coverage Level](../glossary/coverage-level.md)

---

## Navigation

- [Return to Entities Index](./index.md)
- [Return to Bundle Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
- [View Relationships](../relationships/index.md)
