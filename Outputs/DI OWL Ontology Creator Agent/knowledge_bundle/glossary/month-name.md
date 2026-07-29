---
title: Month Name
type: glossary
description: Name of the calendar month for the date
resource: glossary
tags: [glossary, date, month, calendar]
timestamp: 2026-07-28T00:00:00Z
---

# Month Name

## Business Definition

Name of the calendar month for the date.

## Business Meaning

Month Name provides the textual representation of the calendar month, enabling month-based reporting and analysis. It supports monthly trending, seasonal analysis, and month-over-month comparisons.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_date  
**Source Column**: month_name  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Month Name  
**Data Type**: Character Varying(12)  
**Confidence Score**: 1.00

## Synonyms

- Calendar Month
- Month

## Related Concepts

- [Date](./date.md)
- [Full Date](./full-date.md)
- [Calendar Year](./calendar-year.md)

## Usage Context

Month Name is used to:
- Display month labels in reports
- Enable monthly aggregation and trending
- Support seasonal analysis
- Facilitate month-based filtering

## Example Values

- January
- February
- March
- December

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Date (ENT003)  
**Attribute**: ATTR016
