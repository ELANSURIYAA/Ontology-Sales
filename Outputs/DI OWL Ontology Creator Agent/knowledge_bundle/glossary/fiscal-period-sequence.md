---
title: Fiscal Period Sequence
type: glossary
description: Sequential number representing the fiscal reporting period in ordered time analysis
resource: glossary
tags: [date, fiscal, period, sequence, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Fiscal Period Sequence

## Business Definition

Sequential number representing the fiscal reporting period in ordered time analysis.

---

## Business Meaning

Fiscal Period Sequence provides a numeric ordering of fiscal periods, enabling time-series analysis, trend calculations, and sequential period comparisons. This attribute facilitates ordered temporal analysis independent of date formats.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_date  
**Source Column:** fiscal_period_seq  
**Data Type:** Integer  
**Entity:** [Date](../entities/date.md)  
**Attribute:** Fiscal Period Sequence  
**Confidence Score:** 1.00

---

## Related Concepts

- [Date](./date.md) - Parent entity
- [Fiscal Year](./fiscal-year.md) - Annual period
- [Fiscal Quarter](./fiscal-quarter.md) - Quarterly period

---

## Usage Context

Fiscal Period Sequence is used to:
- Enable ordered time-series analysis
- Support sequential period comparisons
- Calculate period-over-period changes
- Facilitate trend analysis and forecasting

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/date.md)
- [Return to Bundle Index](../index.md)
