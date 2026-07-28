---
title: Date Key
type: glossary
description: Encoded key that uniquely identifies a reporting date in the date dimension
resource: glossary
tags: [glossary, date, key, identifier, surrogate-key]
timestamp: 2026-07-28T00:00:00Z
---

# Date Key

## Business Definition

Encoded key that uniquely identifies a reporting date in the date dimension.

---

## Business Meaning

Date Key is a system-generated unique identifier used to establish relationships between the date dimension and fact records. It serves as the primary key for date records and enables efficient data integration and referential integrity for time-based analysis.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_date

**Source Column**: date_key

**Entity**: [Date](../entities/date.md)

**Attribute**: Date Key

**Data Type**: Integer

**Confidence Score**: 0.95

---

## Related Concepts

- [Date](date.md)
- [Booking Date Key](booking-date-key.md)
- [Booking Transaction](booking-transaction.md)

---

## Usage Context

Date Key is used to:
- Uniquely identify date records
- Link booking transactions to dates
- Maintain referential integrity
- Enable efficient joins between fact and dimension tables
- Support data warehouse operations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Date](../entities/date.md)
- [Back to Main Index](../index.md)
