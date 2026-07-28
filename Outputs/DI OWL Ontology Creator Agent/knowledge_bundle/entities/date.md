---
title: Date
type: entity
description: Business entity representing calendar and fiscal date attributes for time-based analysis
resource: entities
tags: [entity, dimension, date, time, calendar, fiscal]
timestamp: 2026-07-28T00:00:00Z
---

# Date

## Business Definition

Stores calendar and fiscal date attributes used to analyze bookings over time. The Date entity enables time-based analysis across calendar and fiscal periods, supporting trending, period-over-period comparisons, and fiscal reporting.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_date  
**Entity Type**: Dimension  
**Entity ID**: ENT003

---

## Attributes

- **Date Key** (date_key) - integer, NOT NULL
- **Full Date** (full_date) - date, NOT NULL
- **Month Name** (month_name) - character varying(12), NULL
- **Calendar Year** (calendar_year) - integer, NULL
- **Fiscal Year** (fiscal_year) - character varying(6), NULL
- **Fiscal Quarter** (fiscal_quarter) - character varying(10), NULL
- **Fiscal Period Sequence** (fiscal_period_seq) - integer, NULL

---

## Primary Keys

- **Date Key** (date_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- [Date to Booking Transaction](../relationships/date-to-booking-transaction.md) - Links dates to booking transactions (One-to-Many)

---

## Measures

Dates are used to analyze time-based trends for all booking measures:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Discount Percentage](../measures/discount-percentage.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)

---

## Related Concepts

### Related Entities
- [Booking Transaction](booking-transaction.md) - Booking transactions occurring on specific dates
- [Customer](customer.md) - Customer bookings analyzed over time
- [Product](product.md) - Product bookings analyzed over time

### Related Glossary Terms
- [Date](../glossary/date.md)
- [Date Key](../glossary/date-key.md)
- [Full Date](../glossary/full-date.md)
- [Month Name](../glossary/month-name.md)
- [Calendar Year](../glossary/calendar-year.md)
- [Fiscal Year](../glossary/fiscal-year.md)
- [Fiscal Quarter](../glossary/fiscal-quarter.md)
- [Fiscal Period Sequence](../glossary/fiscal-period-sequence.md)

### Related Domains
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Uniqueness**: Each date record is uniquely identified by Date Key
2. **Date Representation**: Full Date contains the actual calendar date
3. **Calendar Attributes**: Calendar Year and Month Name support calendar-based reporting
4. **Fiscal Attributes**: Fiscal Year and Fiscal Quarter support fiscal period reporting
5. **Period Sequencing**: Fiscal Period Sequence enables ordered time-series analysis
6. **Time Granularity**: Date dimension supports daily-level analysis with aggregation to higher periods

---

## Usage Examples

### Fiscal Period Reporting
Analyze booking amounts by fiscal year and fiscal quarter to support financial reporting and planning.

### Trend Analysis
Use Fiscal Period Sequence to create time-series visualizations and identify booking trends over time.

### Year-over-Year Comparison
Compare booking performance across calendar or fiscal years to measure growth.

### Seasonal Analysis
Analyze booking patterns by month name to identify seasonal trends and optimize sales strategies.

### Period-to-Date Calculations
Calculate quarter-to-date and year-to-date booking amounts using date attributes.

---

## Data Quality Notes

- Date Key is mandatory and serves as the primary key
- Full Date is mandatory and represents the actual calendar date
- Calendar and fiscal attributes should be consistently populated
- Fiscal Period Sequence should be sequential and continuous
- Date dimension should contain records for all relevant business dates
- Future dates may be included to support forecasting and planning

---

## Navigation

- [View Entity Index](index.md)
- [View Related Relationships](../relationships/index.md)
- [View Related Measures](../measures/index.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Entity ID**: ENT003  
**Domain**: Sales Bookings and Revenue Analytics  
**Entity Type**: Dimension  
**Attribute Count**: 7  
**Relationship Count**: 1  
**Last Updated**: 2026-07-28T00:00:00Z
