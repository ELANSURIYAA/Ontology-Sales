---
title: Auto Renew Flag
type: glossary
description: Indicator showing whether the contract is set to renew automatically at the end of its term
resource: glossary
tags: [auto-renew, flag, renewal, indicator]
timestamp: 2024-01-15T00:00:00Z
---

# Auto Renew Flag

## Business Definition

Indicator showing whether the contract is set to renew automatically at the end of its term. This flag identifies contracts with automatic renewal provisions.

---

## Business Meaning

Auto Renew Flag is a boolean indicator that identifies whether a contract has automatic renewal provisions. When set to true (1), the contract will automatically renew at the end of its term unless explicitly cancelled. When false (0), the contract requires active renewal action. This attribute is critical for renewal forecasting, customer retention planning, and revenue predictability.

---

## Technical Mapping

**Source Field**: contracts.auto_renew_flag  
**Data Type**: Boolean/Integer (0 or 1)  
**Dimension**: Yes

---

## Synonyms

- Auto Renewal Flag
- Automatic Renewal Indicator
- Renewal Automation Flag
- Auto Renew Indicator

---

## Related Concepts

- [Contract Type](contract-type.md)
- [Term Months](term-months.md)
- [Coverage Level](coverage-level.md)
- [Contract](../entities/contracts.md)

---

## Usage Context

Auto Renew Flag is used in:
- Renewal forecasting
- Customer retention planning
- Revenue predictability analysis
- Contract management
- Churn risk assessment

---

## Navigation

- [Return to Glossary Index](index.md)
- [View Contract Entity](../entities/contracts.md)
- [View Contracts Domain](../domains/contracts.md)
