---
title: Contract Term Months
type: glossary
description: Indicates the duration of the contract in months
resource: glossary
tags: [contract, term, duration, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Term Months

## Business Definition

Indicates the duration of the contract in months.

---

## Business Meaning

Contract Term Months specifies the commitment period for a commercial agreement, measured in months. This attribute is critical for calculating annualized contract values and understanding customer commitment lengths.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_contract  
**Source Column:** term_months  
**Data Type:** Integer  
**Entity:** [Contract](../entities/contract.md)  
**Attribute:** Contract Term Months  
**Confidence Score:** 1.00

---

## Related Concepts

- [Contract](./contract.md) - Parent entity
- [Contract Type](./contract-type.md) - Type of agreement
- [Annual Contract Value USD](./annual-contract-value-usd.md) - Calculated using term months
- [Total Contract Value USD](./total-contract-value-usd.md) - Total value over term

---

## Usage Context

Contract Term Months is used to:
- Define the commitment period for agreements
- Calculate annualized contract values
- Analyze contract length patterns
- Support renewal planning and forecasting

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/contract.md)
- [Return to Bundle Index](../index.md)
