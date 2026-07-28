---
title: Auto Renew Flag
type: glossary
description: Indicates whether the contract is set to renew automatically at the end of its term
resource: glossary
tags: [glossary, contract, renewal, auto-renew, flag]
timestamp: 2026-07-28T00:00:00Z
---

# Auto Renew Flag

## Business Definition

Indicates whether the contract is set to renew automatically at the end of its term.

---

## Business Meaning

Auto Renew Flag is a binary indicator that specifies whether a contract will automatically renew when it reaches the end of its term. Contracts with auto-renewal enabled continue without requiring explicit customer action, improving retention and reducing administrative overhead. This flag is critical for forecasting recurring revenue and managing customer retention strategies.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract

**Source Column**: auto_renew_flag

**Entity**: [Contract](../entities/contract.md)

**Attribute**: Auto Renew Flag

**Data Type**: Character(1)

**Confidence Score**: 1.00

---

## Related Concepts

- [Contract](contract.md)
- [Contract Key](contract-key.md)
- [Contract Term Months](contract-term-months.md)
- [Renewal Indicator](renewal-indicator.md)

---

## Usage Context

Auto Renew Flag is used to:
- Identify contracts with automatic renewal
- Forecast recurring revenue
- Manage renewal processes
- Analyze retention strategies
- Support customer lifecycle management
- Reduce churn risk

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Contract](../entities/contract.md)
- [Back to Main Index](../index.md)
