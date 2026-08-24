---
title: Dates
type: entity
description: Provides calendar and fiscal time attributes used to analyze bookings across reporting periods, years, quarters, and months
resource: entities
tags: [dates, dimension, time, fiscal-period, calendar]
timestamp: 2026-07-28T00:00:00Z
---

# Dates

## Business Definition

The Dates entity represents the time dimension table that provides calendar and fiscal time attributes. Each record contains date identifiers, calendar attributes, and fiscal period classifications. This entity enables time-based analysis of booking transactions across reporting periods, years, quarters, and months, supporting both calendar and fiscal year reporting requirements.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_date

**Source Schema**: quotetobooking

**Entity Type**: Dimension Table (Time Dimension)

---

## Attributes

- date_key
- full_date
- month_name
- calendar_year
- fiscal_year
- fiscal_quarter
- fiscal_period_seq

---

## Primary Keys

- date_key

---

## Foreign Keys

None

---

## Relationships

- [Bookings to Dates](../relationships/bookings-to-dates.md)

---

## Measures

All booking-related measures can be analyzed by time attributes:
- [Booking Count](../measures/booking-count.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

---

## Related Concepts

- [Fiscal Period](../glossary/fiscal-period.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

1. **Unique Date Key**: Each date record must have a unique date_key in YYYYMMDD format
2. **Date Key Format**: date_key is an intelligent key in YYYYMMDD format for easy date range filtering
3. **Calendar Attributes**: Calendar year and month name provide standard calendar-based reporting
4. **Fiscal Attributes**: Fiscal year, quarter, and period support fiscal reporting requirements
5. **Sequential Periods**: fiscal_period_seq provides sequential ordering of fiscal periods for trend analysis

---

## Attribute Definitions

### date_key
Intelligent date key in YYYYMMDD form used to join booking records to the date dimension. Provides efficient date range filtering and sorting.

### full_date
Actual calendar date represented by the date record. Provides the standard date value for temporal analysis.

### month_name
Name of the calendar month for the date. Enables month-based reporting and seasonal analysis.

### calendar_year
Calendar year associated with the date. Supports calendar year-based reporting and year-over-year comparisons.

### fiscal_year
Fiscal year used for financial and sales reporting. Aligns with organizational fiscal calendar requirements.

### fiscal_quarter
Fiscal quarter used for period-based reporting and analysis. Supports quarterly business reviews and planning cycles.

### fiscal_period_seq
Sequential number representing the fiscal reporting period in order. Enables trend analysis and period-over-period comparisons.

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Usage Examples

### Calendar Year Analysis
- Analyze booking trends by calendar year
- Compare year-over-year performance
- Track seasonal booking patterns

### Fiscal Year Analysis
- Report bookings by fiscal year
- Track fiscal year quota attainment
- Support fiscal year planning and forecasting

### Fiscal Quarter Analysis
- Analyze quarterly booking trends
- Track quarter-over-quarter growth
- Support quarterly business reviews

### Month Analysis
- Track monthly booking patterns
- Identify seasonal trends
- Support monthly forecasting

### Period Sequence Analysis
- Analyze booking trends over sequential periods
- Calculate period-over-period growth rates
- Support time series analysis

---

## Data Quality Checks

- date_key is unique and not null
- date_key follows YYYYMMDD format
- full_date is not null and is a valid date
- month_name is a valid month name
- calendar_year is a valid four-digit year
- fiscal_year is a valid fiscal year designation
- fiscal_quarter is a valid quarter (Q1, Q2, Q3, Q4)
- fiscal_period_seq is sequential and not null
