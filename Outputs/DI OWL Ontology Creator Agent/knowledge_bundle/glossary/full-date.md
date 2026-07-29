---
title: Full Date
type: glossary
description: Actual calendar date represented by the date record
resource: glossary
tags: [glossary, date, calendar]
timestamp: 2026-07-28T00:00:00Z
---

# Full Date

## Business Definition

Actual calendar date represented by the date record.

## Business Meaning

Full Date is the actual calendar date value used for date-based filtering, sorting, and display. It represents a specific day and is the foundation for all other date attributes in the dimension.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_date  
**Source Column**: full_date  
**Entity**: [Date](../entities/date.md)  
**Attribute**: Full Date  
**Data Type**: Date  
**Confidence Score**: 1.00

## Synonyms

- Calendar Date
- Transaction Date
- Actual Date

## Related Concepts

- [Date](./date.md)
- [Date Key](./date-key.md)
- [Booking Date Key](./booking-date-key.md)

## Usage Context

Full Date is used to:
- Filter transactions by specific dates
- Display human-readable dates in reports
- Calculate date-based metrics
- Support date range queries

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Date (ENT003)  
**Attribute**: ATTR015
