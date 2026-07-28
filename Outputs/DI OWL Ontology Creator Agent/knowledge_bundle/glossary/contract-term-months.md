---
title: Contract Term Months
type: glossary
description: Duration of the contract in months
resource: glossary
tags: [glossary, contract, term, duration, months]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Term Months

## Business Definition

Indicates the duration of the contract in months.

---

## Business Meaning

Contract Term Months specifies the length of the contractual commitment between the organization and the customer. This duration determines the period over which the customer is committed to the agreement and influences revenue recognition, renewal timing, and contract value calculations. Common terms include 12 months (annual), 24 months, 36 months, or other custom durations.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract

**Source Column**: term_months

**Entity**: [Contract](../entities/contract.md)

**Attribute**: Contract Term Months

**Data Type**: Integer

**Confidence Score**: 1.00

---

## Related Concepts

- [Contract](contract.md)
- [Contract Key](contract-key.md)
- [Annual Contract Value USD](annual-contract-value-usd.md)
- [Total Contract Value USD](total-contract-value-usd.md)
- [Auto Renew Flag](auto-renew-flag.md)

---

## Usage Context

Contract Term Months is used to:
- Define contract duration
- Calculate annualized contract values
- Determine renewal timing
- Support revenue recognition
- Analyze contract term preferences
- Forecast contract expirations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Contract](../entities/contract.md)
- [Back to Main Index](../index.md)
