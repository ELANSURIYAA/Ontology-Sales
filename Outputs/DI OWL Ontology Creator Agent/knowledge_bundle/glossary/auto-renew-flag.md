---
title: Auto Renew Flag
type: glossary
description: Indicates whether the contract is set to renew automatically at the end of its term
resource: glossary
tags: [contract, renewal, flag, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Auto Renew Flag

## Business Definition

Indicates whether the contract is set to renew automatically at the end of its term.

---

## Business Meaning

Auto Renew Flag is a binary indicator that determines whether a contract will automatically continue for another term upon expiration. This attribute is critical for forecasting recurring revenue and managing customer retention.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_contract  
**Source Column:** auto_renew_flag  
**Data Type:** Character(1)  
**Entity:** [Contract](../entities/contract.md)  
**Attribute:** Auto Renew Flag  
**Confidence Score:** 1.00

---

## Related Concepts

- [Contract](./contract.md) - Parent entity
- [Contract Term Months](./contract-term-months.md) - Renewal term length
- [Renewal Indicator](./renewal-indicator.md) - Booking renewal classification
- [Booking Type](./booking-type.md) - New vs renewal bookings

---

## Usage Context

Auto Renew Flag is used to:
- Identify contracts with automatic renewal provisions
- Forecast recurring revenue streams
- Support customer retention analysis
- Plan renewal engagement strategies

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/contract.md)
- [Return to Bundle Index](../index.md)
