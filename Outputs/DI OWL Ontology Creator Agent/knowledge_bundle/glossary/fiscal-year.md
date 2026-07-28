---
title: Fiscal Year
type: glossary
description: Fiscal year used by the business for financial and performance reporting
resource: glossary
tags: [glossary, date, fiscal-year, financial]
timestamp: 2026-07-28T00:00:00Z
---

# Fiscal Year

## Business Definition

Fiscal year used by the business for financial and performance reporting.

---

## Business Meaning

Fiscal Year represents the organization's financial reporting year, which may differ from the calendar year. It enables fiscal period reporting, budget tracking, and financial performance analysis aligned with the organization's fiscal calendar.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_date  
**Source Column**: fiscal_year  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Fiscal Year  
**Data Type**: character varying(6)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Financial Year
- FY

---

## Related Concepts

### Related Entities
- [Date](../entities/date.md)

### Related Attributes
- [Calendar Year](calendar-year.md)
- [Fiscal Quarter](fiscal-quarter.md)
- [Fiscal Period Sequence](fiscal-period-sequence.md)

---

## Usage Context

Fiscal Year is used to:
- Support fiscal period reporting
- Enable budget tracking
- Align with financial planning cycles

---

## Examples

- FY2024
- FY2025

---

## Navigation

- [View Glossary Index](index.md)
- [View Date Entity](../entities/date.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Date  
**Source Attribute**: Fiscal Year  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
