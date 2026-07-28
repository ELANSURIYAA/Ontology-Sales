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

---

## Business Meaning

Month Name provides the textual name of the calendar month (e.g., January, February) associated with the date. This enables month-based reporting, seasonal analysis, and human-readable date displays.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_date  
**Source Column**: month_name  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Month Name  
**Data Type**: character varying(12)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Calendar Month
- Month

---

## Related Concepts

### Related Entities
- [Date](../entities/date.md)

### Related Attributes
- [Full Date](full-date.md)
- [Calendar Year](calendar-year.md)

---

## Usage Context

Month Name is used to:
- Support month-based reporting
- Enable seasonal analysis
- Provide human-readable month identification

---

## Examples

- January
- February
- March
- December

---

## Navigation

- [View Glossary Index](index.md)
- [View Date Entity](../entities/date.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Date  
**Source Attribute**: Month Name  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
