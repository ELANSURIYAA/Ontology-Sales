---
title: Fiscal Period Sequence
type: glossary
description: Sequential number representing the fiscal reporting period in chronological order
resource: glossary
tags: [fiscal-period-seq, period, sequence, time]
timestamp: 2024-01-15T00:00:00Z
---

# Fiscal Period Sequence

## Business Definition

Sequential number representing the fiscal reporting period in chronological order. This provides a numeric sequence for ordering fiscal periods.

---

## Business Meaning

Fiscal Period Sequence is a sequential integer that represents fiscal reporting periods in chronological order. This enables easy sorting and period-over-period calculations without complex date logic. For example, if Period 1 = January 2023, Period 2 = February 2023, etc., the sequence provides a simple numeric ordering for trend analysis and period comparisons.

---

## Technical Mapping

**Source Field**: dates.fiscal_period_seq  
**Data Type**: Integer  
**Dimension**: Yes

---

## Synonyms

- Period Sequence
- Fiscal Period Number
- Period Seq
- Sequential Period

---

## Related Concepts

- [Fiscal Year](fiscal-year.md)
- [Fiscal Quarter](fiscal-quarter.md)
- [Calendar Year](calendar-year.md)
- [Date](../entities/dates.md)

---

## Usage Context

Fiscal Period Sequence is used in:
- Period-over-period calculations
- Chronological ordering
- Trend analysis
- Period-based filtering
- Sequential period comparisons

---

## Navigation

- [Return to Glossary Index](index.md)
- [View Date Entity](../entities/dates.md)
- [View Dates Domain](../domains/dates.md)
