---
title: Fiscal Period Sequence
type: glossary
description: Sequential number representing the fiscal reporting period in ordered time analysis
resource: glossary
tags: [glossary, date, fiscal, period, sequence]
timestamp: 2026-07-28T00:00:00Z
---

# Fiscal Period Sequence

## Business Definition

Sequential number representing the fiscal reporting period in ordered time analysis.

## Business Meaning

Fiscal Period Sequence provides a continuous numeric sequence for fiscal periods, enabling ordered time-series analysis, period-over-period calculations, and trending. It simplifies temporal calculations and comparisons across fiscal periods.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_date  
**Source Column**: fiscal_period_seq  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Fiscal Period Sequence  
**Data Type**: Integer  
**Confidence Score**: 1.00

## Synonyms

- Period Sequence
- Fiscal Period Number
- Period Index

## Related Concepts

- [Date](./date.md)
- [Fiscal Year](./fiscal-year.md)
- [Fiscal Quarter](./fiscal-quarter.md)

## Usage Context

Fiscal Period Sequence is used to:
- Enable ordered time-series analysis
- Calculate period-over-period changes
- Support trending and forecasting
- Simplify temporal calculations

## Example Values

- 1 (First fiscal period)
- 2 (Second fiscal period)
- 12 (Twelfth fiscal period)

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Date (ENT003)  
**Attribute**: ATTR020
