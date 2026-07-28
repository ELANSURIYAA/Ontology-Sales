---
title: Date to Booking Transaction
type: relationship
description: One-to-Many relationship linking dates to booking transactions
resource: relationships
tags: [relationship, foreign-key, date, booking-transaction, time]
timestamp: 2026-07-28T00:00:00Z
---

# Date to Booking Transaction

## Business Description

This relationship links date records to booking transactions, enabling time-based analysis of bookings by fiscal year, fiscal quarter, calendar year, and month.

---

## Relationship Details

**Source Entity**: [Date](../entities/date.md)

**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Relationship Type**: Foreign Key

**Cardinality**: One-to-Many

**Confidence Score**: 1.00

---

## Technical Mapping

**Parent Table**: QuoteToBooking.dim_date

**Parent Column**: date_key

**Child Table**: QuoteToBooking.fact_bookings

**Child Column**: date_key

---

## Cardinality Explanation

- **One Date** can be associated with **Many Booking Transactions**
- **Each Booking Transaction** must reference **exactly one Date**

This relationship enables:
- Analysis of booking trends over time
- Evaluation of fiscal and calendar period performance
- Measurement of seasonal patterns
- Time-series analysis and forecasting

---

## Business Rules

1. Every booking transaction must reference a valid date
2. A date can be associated with zero or many booking transactions
3. Date Key is the foreign key in the booking transaction fact table
4. The relationship is mandatory on the booking transaction side
5. The relationship supports referential integrity

---

## Related Concepts

- [Date](../glossary/date.md)
- [Date Key](../glossary/date-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Booking Date Key](../glossary/booking-date-key.md)
- [Fiscal Year](../glossary/fiscal-year.md)
- [Fiscal Quarter](../glossary/fiscal-quarter.md)

---

## Usage Examples

**Analyze bookings by fiscal year**:
- Compare year-over-year booking performance
- Measure annual growth rates

**Analyze bookings by fiscal quarter**:
- Track quarterly booking trends
- Evaluate seasonal patterns

**Analyze bookings by month**:
- Identify monthly booking patterns
- Compare month-over-month performance

**Time-series analysis**:
- Calculate moving averages
- Perform trend analysis
- Generate forecasts

---

## Navigation

- [Back to Relationships Index](index.md)
- [View Source Entity: Date](../entities/date.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
