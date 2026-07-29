---
title: Time Management Domain
type: domain
description: Calendar and fiscal time attributes used to analyze bookings across dates, months, years, quarters, and fiscal periods
resource: domains
tags: [okf, domain, time-management, date, fiscal-calendar]
timestamp: 2026-07-28T00:00:00Z
---

# Time Management Domain

## Business Definition

The Time Management domain encompasses calendar and fiscal time attributes used to analyze bookings across dates, months, years, quarters, and fiscal periods. This domain provides the temporal context necessary for time-based sales analytics and trend analysis.

---

## Business Purpose

This domain enables business users to:

- Analyze sales performance over time
- Track revenue trends by fiscal period
- Compare year-over-year and quarter-over-quarter performance
- Monitor monthly booking patterns
- Support fiscal reporting and planning
- Enable time-based forecasting
- Analyze seasonality and trends

---

## Domain Scope

### Included
- Calendar date attributes
- Fiscal year and quarter attributes
- Month and year classifications
- Fiscal period sequencing
- Date hierarchies (Year → Quarter → Month → Date)

### Excluded
- Time of day (hours, minutes, seconds)
- Timezone information
- Holiday calendars
- Working day versus non-working day flags
- Week-based attributes

---

## Related Entities

### Primary Entities
- [Date Dimension](../entities/date-dimension.md)

---

## Related Measures

All sales and revenue measures can be analyzed by time attributes:

- [Quantity Sold](../measures/quantity-sold.md) by time period
- [Booking Amount USD](../measures/booking-amount-usd.md) by time period
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md) by time period
- [Total Contract Value USD](../measures/total-contract-value-usd.md) by time period
- [Unit List Price USD](../measures/unit-list-price-usd.md) by time period
- [Discount Percentage](../measures/discount-percentage.md) by time period

---

## Related Relationships

- [Date to Booking](../relationships/date-to-booking.md)

---

## Key Business Concepts

### Calendar Date
Actual calendar date represented by the date record, serving as the foundation for all time-based analysis.

### Fiscal Year
Fiscal year used for business reporting and financial analysis. The fiscal year may differ from the calendar year depending on organizational fiscal calendar.

### Fiscal Quarter
Fiscal quarter associated with the date for reporting purposes, enabling quarterly performance tracking and analysis.

### Fiscal Period Sequence
Sequential number representing the fiscal period order in the reporting calendar, enabling period-over-period comparisons and trending.

### Time Hierarchy
The date dimension supports hierarchical analysis:
- **Level 1**: Fiscal Year (highest level)
- **Level 2**: Fiscal Quarter
- **Level 3**: Month
- **Level 4**: Date (lowest level)

---

## Business Rules

1. Every date record must have a unique Date Key (surrogate key)
2. Every date record must have a unique Full Date (business key)
3. Calendar Year must be a valid four-digit year
4. Fiscal Year should be populated for all dates
5. Fiscal Quarter should be populated for all dates
6. Month Name should match the calendar month
7. Fiscal Period Sequence should be sequential and continuous

---

## Analytical Use Cases

### Trend Analysis
- Track revenue and booking trends over time
- Analyze growth rates period-over-period
- Identify seasonal patterns and cycles
- Monitor long-term performance trends

### Fiscal Reporting
- Report revenue by fiscal year and quarter
- Compare fiscal period performance
- Track fiscal year-to-date metrics
- Support fiscal planning and budgeting

### Comparative Analysis
- Compare year-over-year performance
- Analyze quarter-over-quarter changes
- Compare month-over-month trends
- Benchmark current versus prior periods

### Seasonality Analysis
- Identify seasonal booking patterns
- Analyze monthly and quarterly seasonality
- Support seasonal forecasting
- Plan for seasonal capacity needs

### Time-Based Forecasting
- Forecast future bookings based on historical trends
- Project fiscal year and quarter performance
- Predict seasonal variations
- Support pipeline and quota planning

---

## Data Quality Metrics

### Completeness
- Date Key must be populated for all records
- Full Date must be populated for all records
- Calendar Year must be populated for all records
- Fiscal Year should be populated (>99% target)
- Fiscal Quarter should be populated (>99% target)
- Month Name should be populated (>99% target)

### Accuracy
- Date Key must be unique
- Full Date must be unique
- Calendar Year must be valid four-digit year
- Fiscal Year must follow organizational fiscal calendar
- Fiscal Quarter must align with Fiscal Year
- Month Name must match calendar month

### Consistency
- Fiscal attributes must align with organizational fiscal calendar
- Date hierarchies must be logically consistent
- Fiscal Period Sequence must be sequential
- Date dimension must cover all booking transaction dates

---

## Technical Implementation

### Source System
- **Schema**: quotetobooking
- **Table**: dim_date
- **Primary Key**: date_key (surrogate key)
- **Business Key**: full_date
- **Type**: Static Dimension (pre-populated with date range)

### Key Attributes
- Date Key (Primary Key)
- Full Date (Business Key)
- Month Name
- Calendar Year
- Fiscal Year
- Fiscal Quarter
- Fiscal Period Sequence

### Hierarchy Structure
```
Fiscal Year
└── Fiscal Quarter
    └── Month Name
        └── Full Date
```

---

## Semantic Links

### Related Domains
- [Sales Transactions](sales-transactions.md)
- [Revenue Metrics](revenue-metrics.md)
- [Contract Management](contract-management.md)

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

## Navigation

- [Back to Domains Index](index.md)
- [Back to Bundle Index](../index.md)
