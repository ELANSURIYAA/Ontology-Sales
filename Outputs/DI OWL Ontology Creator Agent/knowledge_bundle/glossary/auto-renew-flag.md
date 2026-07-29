---
title: Auto Renew Flag
type: glossary
description: Indicates whether the contract is set to renew automatically at the end of its term
resource: glossary
tags: [glossary, contract, renewal, flag]
timestamp: 2026-07-28T00:00:00Z
---

# Auto Renew Flag

## Business Definition

Indicates whether the contract is set to renew automatically at the end of its term.

## Business Meaning

The Auto Renew Flag identifies contracts that will automatically renew without requiring explicit customer action or new sales activity. This attribute is critical for forecasting recurring revenue, managing renewal processes, and identifying contracts that require proactive renewal management.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract  
**Source Column**: auto_renew_flag  
**Entity**: [Contract](../entities/contract.md)  
**Attribute**: Auto Renew Flag  
**Data Type**: Character(1)  
**Confidence Score**: 1.00

## Synonyms

- Automatic Renewal Indicator
- Auto Renewal Flag
- Renewal Automation Flag

## Related Concepts

- [Contract](./contract.md)
- [Contract Term Months](./contract-term-months.md)
- [Renewal Indicator](./renewal-indicator.md)
- [Booking Type](./booking-type.md)

## Usage Context

Auto Renew Flag is used to:
- Identify contracts with automatic renewal provisions
- Forecast recurring revenue from auto-renewing contracts
- Manage renewal processes and customer communications
- Analyze renewal behavior patterns

## Example Values

- Y (Yes - contract will auto-renew)
- N (No - contract requires manual renewal)

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Contract (ENT001)  
**Attribute**: ATTR004
