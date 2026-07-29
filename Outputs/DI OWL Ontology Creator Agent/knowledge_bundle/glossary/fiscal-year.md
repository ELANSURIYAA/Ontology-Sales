---
title: Fiscal Year
type: glossary
description: Fiscal year used by the business for financial and performance reporting
resource: glossary
tags: [date, fiscal, year, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Fiscal Year

## Business Definition

Fiscal year used by the business for financial and performance reporting.

---

## Business Meaning

Fiscal Year represents the business's financial reporting year, which may differ from the calendar year. This enables alignment with corporate financial planning, budgeting, and performance measurement cycles.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_date  
**Source Column:** fiscal_year  
**Data Type:** Character Varying(6)  
**Entity:** [Date](../entities/date.md)  
**Attribute:** Fiscal Year  
**Confidence Score:** 1.00

---

## Related Concepts

- [Date](./date.md) - Parent entity
- [Calendar Year](./calendar-year.md) - Calendar year
- [Fiscal Quarter](./fiscal-quarter.md) - Quarterly breakdown
- [Fiscal Period Sequence](./fiscal-period-sequence.md) - Period ordering

---

## Usage Context

Fiscal Year is used to:
- Align reporting with business financial cycles
- Enable fiscal year-based analysis
- Support budget and target tracking
- Compare performance across fiscal years

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/date.md)
- [Return to Bundle Index](../index.md)
