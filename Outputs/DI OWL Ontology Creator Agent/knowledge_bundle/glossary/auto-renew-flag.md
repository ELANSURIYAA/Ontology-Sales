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

Auto Renew Flag is a binary indicator that specifies whether a contract will automatically renew when it reaches the end of its term, or whether it requires explicit renewal action. Automatic renewal provisions help ensure continuity of service and reduce churn, while also providing predictable recurring revenue streams.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_contract  
**Source Column**: auto_renew_flag  
**Entity**: [Contract](../entities/contract.md)  
**Attribute**: Auto Renew Flag  
**Data Type**: character(1)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Automatic Renewal Indicator
- Auto Renewal Flag
- Renewal Automation Flag

---

## Related Concepts

### Related Entities
- [Contract](../entities/contract.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Contract Key](contract-key.md)
- [Contract Term Months](contract-term-months.md)
- [Renewal Indicator](renewal-indicator.md)

---

## Usage Context

Auto Renew Flag is used to:
- Identify contracts with automatic renewal provisions
- Forecast recurring revenue
- Plan renewal management activities
- Reduce customer churn risk

---

## Examples

- Y (Yes - contract auto-renews)
- N (No - manual renewal required)

---

## Navigation

- [View Glossary Index](index.md)
- [View Contract Entity](../entities/contract.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Contract  
**Source Attribute**: Auto Renew Flag  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
