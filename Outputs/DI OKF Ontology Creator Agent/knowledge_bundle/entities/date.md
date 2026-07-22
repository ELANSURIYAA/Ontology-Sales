---
title: Date
type: entity
id: ENT003
domain: Sales Bookings and Revenue Analytics
technical_table: QuoteToBooking.dim_date
business_keys:
  - date_key
version: 1.0
status: generated
---

# Date

## Business Definition

Stores calendar and fiscal date attributes used to analyze bookings over time and support period-based reporting.

## Technical Mapping

- Table: `QuoteToBooking.dim_date`
- Primary business key(s): `date_key`

## Attributes

| Attribute | Technical Column | Data Type | Nullable | PK | FK | Description |
| --- | --- | --- | --- | --- | --- | --- |
| Date Key | date_key | integer | No | Yes | No | Encoded key that uniquely identifies a date record in the date dimension. |
| Full Date | full_date | date | No | No | No | Calendar date represented by the date dimension record. |
| Month Name | month_name | character varying | Yes | No | No | Name of the calendar month for the date. |
| Calendar Year | calendar_year | integer | Yes | No | No | Four-digit calendar year associated with the date. |
| Fiscal Year | fiscal_year | character varying | Yes | No | No | Fiscal year used for business reporting and performance analysis. |
| Fiscal Quarter | fiscal_quarter | character varying | Yes | No | No | Fiscal quarter used for reporting and period-based business analysis. |
| Fiscal Period Sequence | fiscal_period_seq | integer | Yes | No | No | Sequential number representing the order of the fiscal period in the reporting calendar. |

## Keys

- Primary Key: `date_key`
- Referenced by: [Booking Transaction](booking-transaction.md)

## Measures

- No direct measures defined for this entity.

## Relationships

- Parent in [Date to Booking Transaction](../relationships/date-to-booking-transaction.md)

## Related Concepts

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Booking Transaction](booking-transaction.md)
- [Date](../glossary/date.md)
- [Fiscal Year](../glossary/fiscal-year.md)