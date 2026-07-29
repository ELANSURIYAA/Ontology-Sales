---
title: Coverage Level
type: glossary
description: Describes the level of service or support coverage provided under the contract
resource: glossary
tags: [contract, coverage, support, service, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Coverage Level

## Business Definition

Describes the level of service or support coverage provided under the contract.

---

## Business Meaning

Coverage Level defines the tier or extent of service and support provided to customers under their contract. Different coverage levels typically correspond to different service response times, support channels, and service level agreements.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_contract  
**Source Column:** coverage_level  
**Data Type:** Character Varying(20)  
**Entity:** [Contract](../entities/contract.md)  
**Attribute:** Coverage Level  
**Confidence Score:** 1.00

---

## Related Concepts

- [Contract](./contract.md) - Parent entity
- [Contract Type](./contract-type.md) - Type of agreement
- [Contract Term Months](./contract-term-months.md) - Contract duration
- [Booking Transaction](./booking-transaction.md) - Transactions with coverage levels

---

## Usage Context

Coverage Level is used to:
- Define service and support tiers
- Analyze booking performance by coverage level
- Support pricing strategies for different service tiers
- Track service level mix and customer preferences

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/contract.md)
- [Return to Bundle Index](../index.md)
