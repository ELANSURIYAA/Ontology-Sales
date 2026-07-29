---
title: Date
type: entity
description: Calendar and fiscal date attributes used to analyze bookings over time
resource: entities
tags: [date, time, calendar, fiscal, dimension, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Date

## Business Definition

The Date entity stores calendar and fiscal date attributes used to analyze bookings over time. It provides comprehensive temporal context including calendar dates, fiscal periods, quarters, and years. This entity enables time-based analysis and trending of booking performance across multiple time hierarchies.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_date  
**Source Schema**: QuoteToBooking  
**Entity Type**: Dimension  
**Entity ID**: ENT003

---

## Attributes

- **Date Key** - Encoded key that uniquely identifies a reporting date in the date dimension
- **Full Date** - Actual calendar date represented by the date record
- **Month Name** - Name of the calendar month for the date
- **Calendar Year** - Four-digit calendar year associated with the date
- **Fiscal Year** - Fiscal year used by the business for financial and performance reporting
- **Fiscal Quarter** - Fiscal quarter used by the business for periodic reporting and analysis
- **Fiscal Period Sequence** - Sequential number representing the fiscal reporting period in ordered time analysis

---

## Primary Keys

- **Date Key** (date_key) - Surrogate key, Integer, Not Nullable

---

## Foreign Keys

None - This is a dimension entity

---

## Relationships

### Outgoing Relationships

- **[Date to Booking Transaction](../relationships/date-to-booking-transaction.md)** - One-to-Many relationship linking dates to booking transactions

### Related Entities

- **[Booking Transaction](./booking-transaction.md)** - Fact entity containing booking records with date references

---

## Measures

Dates support time-based analysis of all measures:

- **[Booking Amount USD](../measures/booking-amount-usd.md)** - Revenue trending over time
- **[Annual Contract Value USD](../measures/annual-contract-value-usd.md)** - ACV trends by period
- **[Total Contract Value USD](../measures/total-contract-value-usd.md)** - TCV trends by period
- **[Quantity Sold](../measures/quantity-sold.md)** - Volume trends over time
- **[Discount Percentage](../measures/discount-percentage.md)** - Pricing trends by period
- **[Unit List Price USD](../measures/unit-list-price-usd.md)** - Price trends over time

---

## Business Rules

1. Date Key must be unique and not null
2. Full Date must be a valid calendar date
3. Calendar Year must be four-digit integer
4. Fiscal Year must follow company fiscal calendar format
5. Fiscal Quarter must be valid quarter designation (Q1, Q2, Q3, Q4)
6. Fiscal Period Sequence must be sequential and continuous
7. Month Name must be valid calendar month

---

## Analytical Usage

### Calendar Analysis
- Analyze booking performance by calendar year, month, and day
- Track seasonal patterns and trends
- Compare year-over-year calendar performance

### Fiscal Analysis
- Report bookings by fiscal year and quarter
- Track fiscal period performance against targets
- Analyze fiscal year-to-date metrics

### Trend Analysis
- Identify booking trends over time
- Perform period-over-period comparisons
- Track growth rates and momentum

### Seasonal Analysis
- Identify seasonal booking patterns
- Analyze quarter-end and year-end effects
- Track monthly and quarterly cycles

---

## Time Hierarchies

### Calendar Hierarchy
```
Calendar Year
  └─ Month Name
      └─ Full Date
```

### Fiscal Hierarchy
```
Fiscal Year
  └─ Fiscal Quarter
      └─ Fiscal Period Sequence
          └─ Full Date
```

---

## Related Concepts

- **[Booking Transaction](./booking-transaction.md)** - Transactions occurring on specific dates
- **[Contract](./contract.md)** - Contract effective dates and terms
- **[Customer](./customer.md)** - Customer acquisition dates
- **[Sales Representative](./sales-representative.md)** - Sales performance by period

---

## Glossary Terms

- [Date](../glossary/date.md)
- [Date Key](../glossary/date-key.md)
- [Full Date](../glossary/full-date.md)
- [Month Name](../glossary/month-name.md)
- [Calendar Year](../glossary/calendar-year.md)
- [Fiscal Year](../glossary/fiscal-year.md)
- [Fiscal Quarter](../glossary/fiscal-quarter.md)
- [Fiscal Period Sequence](../glossary/fiscal-period-sequence.md)

---

## Attribute Details

| Attribute | Technical Column | Data Type | Nullable | Key Type | Description |
|-----------|-----------------|-----------|----------|----------|-------------|
| Date Key | date_key | integer | No | Primary | Encoded key uniquely identifying date |
| Full Date | full_date | date | No | - | Actual calendar date |
| Month Name | month_name | character varying(12) | Yes | - | Name of calendar month |
| Calendar Year | calendar_year | integer | Yes | - | Four-digit calendar year |
| Fiscal Year | fiscal_year | character varying(6) | Yes | - | Fiscal year designation |
| Fiscal Quarter | fiscal_quarter | character varying(10) | Yes | - | Fiscal quarter designation |
| Fiscal Period Sequence | fiscal_period_seq | integer | Yes | - | Sequential fiscal period number |

---

## Semantic Links

- [Entity Index](./index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Relationship Index](../relationships/index.md)
- [Measure Index](../measures/index.md)
- [Main Index](../index.md)

---

## Metadata

**Entity ID**: ENT003  
**Domain ID**: DOM001  
**Entity Type**: Dimension  
**Technical Table**: QuoteToBooking.dim_date  
**Total Attributes**: 7  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
