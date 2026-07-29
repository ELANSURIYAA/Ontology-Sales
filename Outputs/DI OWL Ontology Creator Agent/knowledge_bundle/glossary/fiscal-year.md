---
title: Fiscal Year
type: glossary
description: Fiscal year used by the business for financial and performance reporting
resource: glossary
tags: [glossary, date, fiscal, year]
timestamp: 2026-07-28T00:00:00Z
---

# Fiscal Year

## Business Definition

Fiscal year used by the business for financial and performance reporting.

## Business Meaning

Fiscal Year represents the company's financial reporting year, which may differ from the calendar year. It is essential for aligning booking analysis with financial reporting periods, budgets, and fiscal targets.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_date  
**Source Column**: fiscal_year  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Fiscal Year  
**Data Type**: Character Varying(6)  
**Confidence Score**: 1.00

## Synonyms

- FY
- Financial Year

## Related Concepts

- [Date](./date.md)
- [Calendar Year](./calendar-year.md)
- [Fiscal Quarter](./fiscal-quarter.md)
- [Fiscal Period Sequence](./fiscal-period-sequence.md)

## Usage Context

Fiscal Year is used to:
- Align reporting with financial periods
- Track fiscal year performance
- Support budget and target comparisons
- Enable fiscal year-over-year analysis

## Example Values

- FY2024
- FY2025
- FY2026

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Date (ENT003)  
**Attribute**: ATTR018
