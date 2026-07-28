---
title: Fiscal Quarter
type: glossary
description: Fiscal quarter used by the business for periodic reporting and analysis
resource: glossary
tags: [glossary, date, fiscal-quarter, financial]
timestamp: 2026-07-28T00:00:00Z
---

# Fiscal Quarter

## Business Definition

Fiscal quarter used by the business for periodic reporting and analysis.

---

## Business Meaning

Fiscal Quarter represents a three-month period within the organization's fiscal year. It enables quarterly performance reporting, trend analysis, and period-over-period comparisons aligned with the organization's fiscal calendar.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_date  
**Source Column**: fiscal_quarter  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Fiscal Quarter  
**Data Type**: character varying(10)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Quarter
- FQ
- Financial Quarter

---

## Related Concepts

### Related Entities
- [Date](../entities/date.md)

### Related Attributes
- [Fiscal Year](fiscal-year.md)
- [Fiscal Period Sequence](fiscal-period-sequence.md)

---

## Usage Context

Fiscal Quarter is used to:
- Support quarterly reporting
- Enable quarter-over-quarter analysis
- Track quarterly performance

---

## Examples

- FY2024 Q1
- FY2024 Q2
- FY2024 Q3
- FY2024 Q4

---

## Navigation

- [View Glossary Index](index.md)
- [View Date Entity](../entities/date.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Date  
**Source Attribute**: Fiscal Quarter  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
