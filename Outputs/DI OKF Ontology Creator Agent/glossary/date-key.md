---
title: Date Key
type: glossary
description: Numeric surrogate key representing a specific calendar date
resource: glossary
tags: [okf, glossary, attribute, date, key]
timestamp: 2026-07-28T00:00:00Z
---

# Date Key

## Business Definition

Numeric surrogate key representing a specific calendar date.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_date  
**Source Column**: date_key  
**Entity**: Date Dimension  
**Attribute**: Date Key

---

## Business Meaning

The Date Key is a system-generated unique identifier used to link booking transactions to their associated date attributes. It serves as the primary key in the Date Dimension and as a foreign key in the Booking Fact table.

---

## Related Concepts

- [Date Dimension](date-dimension.md)
- [Booking Fact](booking-fact.md)

---

## Navigation

- [Back to Glossary Index](index.md)
- [Back to Bundle Index](../index.md)
