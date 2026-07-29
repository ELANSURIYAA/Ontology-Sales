---
title: Full Date
type: glossary
description: Actual calendar date represented by the date record
resource: glossary
tags: [date, calendar, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Full Date

## Business Definition

Actual calendar date represented by the date record.

---

## Business Meaning

Full Date is the actual calendar date value that corresponds to the date record. It provides the specific day for transaction analysis and reporting.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_date  
**Source Column:** full_date  
**Data Type:** Date  
**Entity:** [Date](../entities/date.md)  
**Attribute:** Full Date  
**Confidence Score:** 1.00

---

## Related Concepts

- [Date](./date.md) - Parent entity
- [Date Key](./date-key.md) - Date identifier
- [Calendar Year](./calendar-year.md) - Year component

---

## Usage Context

Full Date is used to:
- Identify specific calendar dates
- Support date-based filtering and analysis
- Enable date range queries
- Provide human-readable date values

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/date.md)
- [Return to Bundle Index](../index.md)
