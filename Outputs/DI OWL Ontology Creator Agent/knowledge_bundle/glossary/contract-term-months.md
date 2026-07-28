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

Contract Term Months specifies the length of time that the contract remains in effect, measured in months. This duration determines the period over which services are provided, revenue is recognized, and contractual obligations are maintained. Contract term is a key factor in calculating annualized contract values and planning renewal activities.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_contract  
**Source Column**: term_months  
**Entity**: [Contract](../entities/contract.md)  
**Attribute**: Contract Term Months  
**Data Type**: integer  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Contract Duration
- Term Length
- Contract Period
- Agreement Term

---

## Related Concepts

### Related Entities
- [Contract](../entities/contract.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Contract Key](contract-key.md)
- [Contract Type](contract-type.md)

### Related Measures
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Usage Context

Contract Term Months is used to:
- Calculate annualized contract values
- Plan renewal activities
- Forecast future revenue
- Analyze contract duration patterns

---

## Examples

- 12 months (annual contract)
- 24 months (two-year contract)
- 36 months (three-year contract)
- 60 months (five-year contract)

---

## Navigation

- [View Glossary Index](index.md)
- [View Contract Entity](../entities/contract.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Contract  
**Source Attribute**: Contract Term Months  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
