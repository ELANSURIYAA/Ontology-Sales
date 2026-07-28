---
title: Fiscal Period Sequence
type: glossary
description: Sequential number representing the fiscal reporting period in ordered time analysis
resource: glossary
tags: [glossary, date, fiscal-period, sequence, time-series]
timestamp: 2026-07-28T00:00:00Z
---

# Fiscal Period Sequence

## Business Definition

Sequential number representing the fiscal reporting period in ordered time analysis.

---

## Business Meaning

Fiscal Period Sequence is a sequential integer that orders fiscal periods chronologically, enabling time-series analysis, trend calculations, and period-over-period comparisons. This numeric sequence facilitates calculations such as moving averages, cumulative totals, and period-based sorting without relying on date arithmetic.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_date

**Source Column**: fiscal_period_seq

**Entity**: [Date](../entities/date.md)

**Attribute**: Fiscal Period Sequence

**Data Type**: Integer

**Confidence Score**: 1.00

---

## Related Concepts

- [Date](date.md)
- [Fiscal Year](fiscal-year.md)
- [Fiscal Quarter](fiscal-quarter.md)

---

## Usage Context

Fiscal Period Sequence is used to:
- Enable ordered time-series analysis
- Support trend calculations
- Facilitate period-over-period comparisons
- Enable moving average calculations
- Support cumulative total calculations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Date](../entities/date.md)
- [Back to Main Index](../index.md)
