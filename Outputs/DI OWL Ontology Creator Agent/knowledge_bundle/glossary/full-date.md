---
title: Full Date
type: glossary
description: Actual calendar date represented by the date record
resource: glossary
tags: [glossary, date, calendar-date]
timestamp: 2026-07-28T00:00:00Z
---

# Full Date

## Business Definition

Actual calendar date represented by the date record.

---

## Business Meaning

Full Date is the actual calendar date value that corresponds to the date record. It provides the specific day for booking transactions and enables date-based filtering, sorting, and analysis.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_date  
**Source Column**: full_date  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Full Date  
**Data Type**: date  
**Nullable**: No  
**Confidence Score**: 1.00

---

## Synonyms

- Calendar Date
- Transaction Date
- Actual Date

---

## Related Concepts

### Related Entities
- [Date](../entities/date.md)

### Related Attributes
- [Date Key](date-key.md)
- [Calendar Year](calendar-year.md)
- [Month Name](month-name.md)

---

## Usage Context

Full Date is used to:
- Identify specific calendar dates
- Filter transactions by date range
- Support date-based reporting
- Enable chronological sorting

---

## Navigation

- [View Glossary Index](index.md)
- [View Date Entity](../entities/date.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Date  
**Source Attribute**: Full Date  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
