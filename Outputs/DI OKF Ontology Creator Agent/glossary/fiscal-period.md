---
title: Fiscal Period
type: glossary
description: Fiscal reporting period used for financial and sales analysis
resource: glossary
tags: [fiscal-period, time, reporting]
timestamp: 2026-07-28T00:00:00Z
---

# Fiscal Period

## Business Definition

Fiscal Period is a fiscal reporting period used for financial and sales analysis. Fiscal periods align with the organization's fiscal calendar and are used for period-based reporting, planning, and performance measurement.

---

## Business Meaning

Fiscal Period is used to:
- Align reporting with the organization's fiscal calendar
- Support period-based performance measurement
- Enable fiscal year and quarter reporting
- Support budgeting and forecasting cycles
- Track performance against fiscal targets
- Enable period-over-period comparisons

Fiscal periods typically include:
- **Fiscal Year**: 12-month fiscal reporting year
- **Fiscal Quarter**: 3-month fiscal reporting quarter (Q1, Q2, Q3, Q4)
- **Fiscal Month**: Monthly fiscal reporting period
- **Fiscal Period Sequence**: Sequential numbering for trend analysis

---

## Technical Mapping

**Source Entity**: [Dates](../entities/dates.md)

**Source Fields**: fiscal_year, fiscal_quarter, fiscal_period_seq

---

## Synonyms

- Reporting Period
- Financial Period
- Fiscal Reporting Period
- Accounting Period
- FY Period

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Transactions analyzed by fiscal period

---

## Related Entities

- [Dates](../entities/dates.md) - Contains fiscal period attributes

---

## Related Measures

All booking measures can be analyzed by fiscal period:
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Total ACV USD](../measures/total-acv-usd.md)

---

## Usage Context

Fiscal Period is used for:
- Financial reporting and compliance
- Quota and target setting
- Performance measurement
- Budget planning and tracking
- Forecasting and projections
- Period-over-period analysis
- Year-end and quarter-end reporting

---

## Business Rules

1. Fiscal periods align with the organization's fiscal calendar
2. Fiscal year may differ from calendar year
3. Fiscal quarters are typically 3 months each
4. Fiscal period sequence enables chronological ordering
5. All transactions are attributed to fiscal periods for reporting

---

## Fiscal Calendar Example

**Fiscal Year 2024:**
- Q1: February - April
- Q2: May - July
- Q3: August - October
- Q4: November - January

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
