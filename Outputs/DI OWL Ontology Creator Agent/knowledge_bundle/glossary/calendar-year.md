---
title: Calendar Year
type: glossary
description: Four-digit calendar year associated with the date
resource: glossary
tags: [date, year, calendar, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Calendar Year

## Business Definition

Four-digit calendar year associated with the date.

---

## Business Meaning

Calendar Year represents the standard Gregorian calendar year (e.g., 2024, 2025) for the date record. This enables year-based analysis and year-over-year comparisons.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_date  
**Source Column:** calendar_year  
**Data Type:** Integer  
**Entity:** [Date](../entities/date.md)  
**Attribute:** Calendar Year  
**Confidence Score:** 1.00

---

## Related Concepts

- [Date](./date.md) - Parent entity
- [Fiscal Year](./fiscal-year.md) - Business fiscal year
- [Month Name](./month-name.md) - Month component

---

## Usage Context

Calendar Year is used to:
- Group transactions by calendar year
- Enable year-over-year analysis
- Support annual reporting
- Provide calendar-based time context

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/date.md)
- [Return to Bundle Index](../index.md)
