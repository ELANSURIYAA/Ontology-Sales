---
title: Bookings to Dates
type: relationship
description: Links booking transactions to time periods
resource: relationships
tags: [bookings, dates, many-to-one, relationship, time]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Dates

## Business Definition

The Bookings to Dates relationship links individual booking transactions to time periods in the date dimension. This relationship enables time-based analysis of booking performance across calendar and fiscal periods, supporting trend analysis, forecasting, and period-based reporting.

---

## Relationship Type

**Many-to-one**

Multiple booking transactions can occur on the same date.

---

## Source Entity

**[Bookings](../entities/bookings.md)**

The fact table containing individual completed sales booking transactions.

---

## Target Entity

**[Dates](../entities/dates.md)**

The time dimension table containing calendar and fiscal time attributes.

---

## Cardinality

**Many Bookings : One Date**

- Each booking transaction references exactly one date record
- Multiple booking transactions can occur on the same date
- Date records exist independently of bookings (complete date range)

---

## Join Specification

### Left Join Key
- **Field**: date_key
- **Entity**: Bookings
- **Type**: Foreign Key

### Right Join Key
- **Field**: date_key
- **Entity**: Dates
- **Type**: Primary Key

### Join Condition
```sql
bookings.date_key = dates.date_key
```

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings

**Target Table**: quotetobooking.dim_date

**Join Column**: date_key

---

## Business Purpose

This relationship enables:

- **Trend Analysis**: Track booking trends over time
- **Fiscal Reporting**: Analyze bookings by fiscal year, quarter, and period
- **Calendar Reporting**: Analyze bookings by calendar year and month
- **Seasonality Analysis**: Identify seasonal booking patterns
- **Period Comparisons**: Compare performance across time periods
- **Forecasting**: Project future bookings based on historical trends

---

## Related Measures

All booking measures can be analyzed by time attributes:
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

1. **Mandatory Relationship**: Every booking must reference a valid date
2. **Referential Integrity**: date_key in bookings must exist in dates dimension
3. **One Date per Booking**: Each booking references exactly one date record
4. **Date Independence**: Date dimension contains complete date range regardless of bookings

---

## Usage Examples

### Fiscal Year Analysis
```sql
SELECT 
    dates.fiscal_year,
    COUNT(bookings.booking_id) as booking_count,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.fiscal_year
```

### Monthly Trend Analysis
```sql
SELECT 
    dates.calendar_year,
    dates.month_name,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.calendar_year, dates.month_name
ORDER BY dates.calendar_year, dates.fiscal_period_seq
```

---

## Data Quality Rules

- date_key in bookings must not be null
- date_key in bookings must reference valid date_key in dates
- date_key must follow YYYYMMDD format
- No orphaned bookings without date references
- Date dimension must contain all dates in the booking date range

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
