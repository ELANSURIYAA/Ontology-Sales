---
title: Date Dimension
type: entity
description: Calendar and fiscal date attributes used to analyze bookings across time periods
resource: entities
tags: [okf, entity, date, dimension, time-management]
timestamp: 2026-07-28T00:00:00Z
---

# Date Dimension

## Business Definition

The Date Dimension stores calendar and fiscal date attributes used to analyze bookings across time periods, fiscal years, quarters, and months. This dimension enables time-based sales analytics and supports fiscal reporting and trend analysis.

---

## Technical Mapping

**Source Schema**: quotetobooking  
**Source Table**: dim_date  
**Entity Type**: Dimension  
**Grain**: One record per calendar date

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

None (this is a dimension table)

---

## Relationships

### Outbound Relationships
- [Date to Booking](../relationships/date-to-booking.md) - One-to-Many relationship to Booking Fact

---

## Measures

All booking measures can be analyzed by time attributes:

- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Related Concepts

### Related Entities
- [Booking Fact](booking-fact.md)

### Related Domains
- [Time Management](../domains/time-management.md)
- [Sales Transactions](../domains/sales-transactions.md)

### Related Glossary Terms
- [Date Dimension](../glossary/date-dimension.md)
- [Date Key](../glossary/date-key.md)
- [Full Date](../glossary/full-date.md)
- [Month Name](../glossary/month-name.md)
- [Calendar Year](../glossary/calendar-year.md)
- [Fiscal Year](../glossary/fiscal-year.md)
- [Fiscal Quarter](../glossary/fiscal-quarter.md)
- [Fiscal Period Sequence](../glossary/fiscal-period-sequence.md)

---

## Business Rules

1. Date Key must be unique and not null
2. Full Date must be unique and not null
3. Calendar Year must be a valid four-digit year
4. Fiscal Year should be populated for all dates
5. Fiscal Quarter should be populated for all dates
6. Month Name should match the calendar month
7. Fiscal Period Sequence should be sequential and continuous

---

## Attribute Details

### date_key
- **Data Type**: integer
- **Nullable**: No
- **Primary Key**: Yes
- **Description**: Numeric date key representing a specific calendar date

### full_date
- **Data Type**: date
- **Nullable**: No
- **Description**: Actual calendar date represented by the date record

### month_name
- **Data Type**: character varying(12)
- **Nullable**: Yes
- **Description**: Name of the calendar month for the date

### calendar_year
- **Data Type**: integer
- **Nullable**: Yes
- **Description**: Four-digit calendar year of the date

### fiscal_year
- **Data Type**: character varying(6)
- **Nullable**: Yes
- **Description**: Fiscal year used for business reporting and financial analysis

### fiscal_quarter
- **Data Type**: character varying(10)
- **Nullable**: Yes
- **Description**: Fiscal quarter associated with the date for reporting purposes

### fiscal_period_seq
- **Data Type**: integer
- **Nullable**: Yes
- **Description**: Sequential number representing the fiscal period order in the reporting calendar

---

## Analytical Use Cases

- Analyze sales performance over time
- Track revenue trends by fiscal period
- Compare year-over-year and quarter-over-quarter performance
- Monitor monthly booking patterns
- Support fiscal reporting and planning
- Enable time-based forecasting

---

## Data Quality Metrics

- **Completeness**: Date Key and Full Date must be 100% populated
- **Uniqueness**: Date Key and Full Date must be unique
- **Validity**: Calendar Year must be valid four-digit year
- **Consistency**: Fiscal attributes must align with organizational fiscal calendar

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Bundle Index](../index.md)
