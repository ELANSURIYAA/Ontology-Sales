---
title: Month Name
type: glossary
description: Name of the calendar month for the date
resource: glossary
tags: [date, month, calendar, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Month Name

## Business Definition

Name of the calendar month for the date.

---

## Business Meaning

Month Name provides the textual name of the calendar month (e.g., January, February) for the date record. This enables month-based grouping and reporting in a human-readable format.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_date  
**Source Column:** month_name  
**Data Type:** Character Varying(12)  
**Entity:** [Date](../entities/date.md)  
**Attribute:** Month Name  
**Confidence Score:** 1.00

---

## Related Concepts

- [Date](./date.md) - Parent entity
- [Calendar Year](./calendar-year.md) - Year component
- [Fiscal Quarter](./fiscal-quarter.md) - Quarterly grouping

---

## Usage Context

Month Name is used to:
- Provide human-readable month identification
- Enable month-based analysis and reporting
- Support seasonal trend analysis
- Group transactions by calendar month

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/date.md)
- [Return to Bundle Index](../index.md)
