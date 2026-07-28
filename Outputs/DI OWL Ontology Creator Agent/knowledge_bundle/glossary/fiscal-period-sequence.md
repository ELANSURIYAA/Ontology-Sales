---
title: Fiscal Period Sequence
type: glossary
description: Sequential number representing the fiscal reporting period in ordered time analysis
resource: glossary
tags: [glossary, date, fiscal-period, sequence, ordering]
timestamp: 2026-07-28T00:00:00Z
---

# Fiscal Period Sequence

## Business Definition

Sequential number representing the fiscal reporting period in ordered time analysis.

---

## Business Meaning

Fiscal Period Sequence is a numeric value that orders fiscal periods chronologically. It enables time-series analysis, trend calculations, and period-over-period comparisons by providing a continuous numeric sequence across fiscal periods.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_date  
**Source Column**: fiscal_period_seq  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Fiscal Period Sequence  
**Data Type**: integer  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Period Sequence
- Fiscal Period Number
- Period Order

---

## Related Concepts

### Related Entities
- [Date](../entities/date.md)

### Related Attributes
- [Fiscal Year](fiscal-year.md)
- [Fiscal Quarter](fiscal-quarter.md)

---

## Usage Context

Fiscal Period Sequence is used to:
- Enable chronological ordering of fiscal periods
- Support time-series analysis
- Calculate period-over-period changes
- Create trend visualizations

---

## Navigation

- [View Glossary Index](index.md)
- [View Date Entity](../entities/date.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Date  
**Source Attribute**: Fiscal Period Sequence  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
