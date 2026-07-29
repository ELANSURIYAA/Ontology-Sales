---
title: Contract Term Months
type: glossary
description: Duration of the contract in months
resource: glossary
tags: [glossary, contract, term, duration]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Term Months

## Business Definition

Indicates the duration of the contract in months.

## Business Meaning

Contract Term Months specifies the length of time for which the contract is valid and the customer is committed. Contract term is a critical factor in calculating annualized contract values (ACV) and total contract values (TCV), and influences renewal timing and revenue recognition patterns.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract  
**Source Column**: term_months  
**Entity**: [Contract](../entities/contract.md)  
**Attribute**: Contract Term Months  
**Data Type**: Integer  
**Confidence Score**: 1.00

## Synonyms

- Contract Duration
- Term Length
- Contract Period
- Subscription Term

## Related Concepts

- [Contract](./contract.md)
- [Contract Type](./contract-type.md)
- [Annual Contract Value USD](./annual-contract-value-usd.md)
- [Total Contract Value USD](./total-contract-value-usd.md)
- [Auto Renew Flag](./auto-renew-flag.md)

## Usage Context

Contract Term Months is used to:
- Calculate annualized contract values (ACV = TCV / Term in Years)
- Determine contract expiration and renewal dates
- Analyze contract length distribution
- Support revenue recognition scheduling

## Example Values

- 12 (1-year contract)
- 24 (2-year contract)
- 36 (3-year contract)
- 60 (5-year contract)

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Contract (ENT001)  
**Attribute**: ATTR003
