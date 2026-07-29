---
title: Date
type: entity
description: Calendar and fiscal date attributes used to analyze bookings over time
resource: entities
tags: [date, time, calendar, fiscal, dimension]
timestamp: 2026-07-28T00:00:00Z
---

# Date

## Business Definition

Stores calendar and fiscal date attributes used to analyze bookings over time. The Date entity enables temporal analysis across calendar years, fiscal periods, quarters, and months, supporting time-based performance tracking and trend analysis.

---

## Entity Identifier

**Entity ID:** ENT003  
**Domain:** [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_date  
**Table Type:** Dimension Table

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

- **Date Key** (date_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- **[Date to Booking Transaction](../relationships/date-to-booking-transaction.md)** - One-to-Many relationship linking dates to booking transactions

---

## Measures

Dates enable time-based analysis of all measures from [Booking Transaction](./booking-transaction.md) entity:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Business Rules

1. Each date must have a unique Date Key
2. Full Date represents the actual calendar date
3. Fiscal Year and Fiscal Quarter align with business reporting periods
4. Fiscal Period Sequence enables ordered time-series analysis
5. Month Name and Calendar Year support calendar-based reporting

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Transactions occurring on specific dates
- [Fiscal Year](../glossary/fiscal-year.md) - Business fiscal year concept
- [Fiscal Quarter](../glossary/fiscal-quarter.md) - Business fiscal quarter concept
- [Calendar Year](../glossary/calendar-year.md) - Standard calendar year

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

## Navigation

- [Return to Entities Index](./index.md)
- [Return to Bundle Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
- [View Relationships](../relationships/index.md)
