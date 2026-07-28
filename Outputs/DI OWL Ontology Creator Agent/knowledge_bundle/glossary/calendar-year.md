---
title: Calendar Year
type: glossary
description: Four-digit calendar year associated with the date
resource: glossary
tags: [glossary, date, year, calendar]
timestamp: 2026-07-28T00:00:00Z
---

# Calendar Year

## Business Definition

Four-digit calendar year associated with the date.

---

## Business Meaning

Calendar Year represents the standard Gregorian calendar year (e.g., 2024, 2025) for the date. It enables year-based reporting, year-over-year comparisons, and annual trend analysis.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_date  
**Source Column**: calendar_year  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Calendar Year  
**Data Type**: integer  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Year
- Calendar Year Number

---

## Related Concepts

### Related Entities
- [Date](../entities/date.md)

### Related Attributes
- [Full Date](full-date.md)
- [Month Name](month-name.md)
- [Fiscal Year](fiscal-year.md)

---

## Usage Context

Calendar Year is used to:
- Support annual reporting
- Enable year-over-year analysis
- Track long-term trends

---

## Examples

- 2024
- 2025
- 2026

---

## Navigation

- [View Glossary Index](index.md)
- [View Date Entity](../entities/date.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Date  
**Source Attribute**: Calendar Year  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
