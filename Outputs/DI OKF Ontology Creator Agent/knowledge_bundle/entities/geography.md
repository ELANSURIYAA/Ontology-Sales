---
title: Geography
type: entity
id: ENT004
domain: Sales Bookings and Revenue Analytics
technical_table: QuoteToBooking.dim_geography
business_keys:
  - geography_key
version: 1.0
status: generated
---

# Geography

## Business Definition

Stores geographic attributes used to analyze bookings across sales regions, theaters, and countries.

## Technical Mapping

- Table: `QuoteToBooking.dim_geography`
- Primary business key(s): `geography_key`

## Attributes

| Attribute | Technical Column | Data Type | Nullable | PK | FK | Description |
| --- | --- | --- | --- | --- | --- | --- |
| Geography Key | geography_key | integer | No | Yes | No | Surrogate key that uniquely identifies a geography record in the geography dimension. |
| Sales Region | region | character varying | Yes | No | No | High-level geographic region used for business reporting and sales analysis. |
| Sales Theater | theater | character varying | Yes | No | No | Intermediate geographic sales area within a region used for operational reporting. |
| Country | country | character varying | Yes | No | No | Country associated with the geography record for booking analysis. |

## Keys

- Primary Key: `geography_key`
- Referenced by: [Booking Transaction](booking-transaction.md)

## Measures

- No direct measures defined for this entity.

## Relationships

- Parent in [Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)

## Related Concepts

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Booking Transaction](booking-transaction.md)
- [Geography](../glossary/geography.md)
- [Country](../glossary/country.md)