---
title: Date
type: entity
description: Calendar and fiscal date attributes used to analyze bookings over time
resource: entities
tags: [entity, dimension, date, time, calendar, fiscal]
timestamp: 2026-07-28T00:00:00Z
---

# Date

## Business Definition

Stores calendar and fiscal date attributes used to analyze bookings over time.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_date

**Source System**: QuoteToBooking

**Entity Type**: Dimension

---

## Attributes

- **Date Key** (date_key): Encoded key that uniquely identifies a reporting date in the date dimension
- **Full Date** (full_date): Actual calendar date represented by the date record
- **Month Name** (month_name): Name of the calendar month for the date
- **Calendar Year** (calendar_year): Four-digit calendar year associated with the date
- **Fiscal Year** (fiscal_year): Fiscal year used by the business for financial and performance reporting
- **Fiscal Quarter** (fiscal_quarter): Fiscal quarter used by the business for periodic reporting and analysis
- **Fiscal Period Sequence** (fiscal_period_seq): Sequential number representing the fiscal reporting period in ordered time analysis

---

## Primary Keys

- **Date Key** (date_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- **[Date to Booking Transaction](../relationships/date-to-booking-transaction.md)**: One-to-Many relationship linking dates to booking transactions

### Related Entities

- [Booking Transaction](booking-transaction.md): Fact entity that references this dimension

---

## Measures

This dimension supports analysis of the following measures:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Concepts

- [Date](../glossary/date.md)
- [Date Key](../glossary/date-key.md)
- [Full Date](../glossary/full-date.md)
- [Month Name](../glossary/month-name.md)
- [Calendar Year](../glossary/calendar-year.md)
- [Fiscal Year](../glossary/fiscal-year.md)
- [Fiscal Quarter](../glossary/fiscal-quarter.md)
- [Fiscal Period Sequence](../glossary/fiscal-period-sequence.md)

---

## Business Rules

1. Date Key is a surrogate key and must be unique
2. Full Date represents the actual calendar date
3. Month Name provides the calendar month name
4. Calendar Year is a four-digit year value
5. Fiscal Year represents the business fiscal year for financial reporting
6. Fiscal Quarter represents the business fiscal quarter
7. Fiscal Period Sequence enables ordered time-series analysis
8. Every booking transaction must reference a valid date
9. Date dimension supports both calendar and fiscal reporting hierarchies

---

## Usage Examples

**Analysis by Fiscal Year**:
- Compare booking revenue across fiscal years
- Analyze year-over-year growth trends
- Measure annual performance against targets

**Analysis by Fiscal Quarter**:
- Track quarterly booking performance
- Analyze seasonal trends
- Compare quarter-over-quarter growth

**Analysis by Calendar Year**:
- Align bookings with calendar-based planning
- Compare calendar year performance
- Support calendar-based forecasting

**Analysis by Month**:
- Identify monthly booking patterns
- Analyze month-over-month trends
- Track monthly performance against quotas

**Time Series Analysis**:
- Use Fiscal Period Sequence for ordered trend analysis
- Calculate moving averages and cumulative totals
- Perform period-over-period comparisons

---

## Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Main Index](../index.md)
- [View Relationships](../relationships/index.md)
- [View Measures](../measures/index.md)
- [View Glossary](../glossary/index.md)
