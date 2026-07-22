---
title: Sales Representative
type: entity
id: ENT007
domain: Sales Bookings and Revenue Analytics
technical_table: QuoteToBooking.dim_sales_rep
business_keys:
  - sales_rep_key
  - rep_id
version: 1.0
status: generated
---

# Sales Representative

## Business Definition

Stores sales representative attributes used to analyze bookings by individual seller, role, team, and covered segment.

## Technical Mapping

- Table: `QuoteToBooking.dim_sales_rep`
- Primary business key(s): `sales_rep_key`, `rep_id`

## Attributes

| Attribute | Technical Column | Data Type | Nullable | PK | FK | Description |
| --- | --- | --- | --- | --- | --- | --- |
| Sales Representative Key | sales_rep_key | integer | No | Yes | No | Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. |
| Sales Representative ID | rep_id | character varying | No | No | No | Business identifier assigned to the sales representative. |
| Sales Representative Name | rep_name | character varying | Yes | No | No | Full name of the sales representative responsible for the customer relationship or sale. |
| Sales Role | sales_role | character varying | Yes | No | No | Job role or selling responsibility of the sales representative. |
| Sales Team | sales_team | character varying | Yes | No | No | Team or organizational unit to which the sales representative belongs. |
| Covered Segment | segment_covered | character varying | Yes | No | No | Customer segment for which the sales representative is responsible. |

## Keys

- Primary Key: `sales_rep_key`
- Alternate Business Key: `rep_id`
- Referenced by: [Booking Transaction](booking-transaction.md)

## Measures

- No direct measures defined for this entity.

## Relationships

- Parent in [Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)

## Related Concepts

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Booking Transaction](booking-transaction.md)
- [Sales Representative](../glossary/sales-representative.md)
- [Sales Role](../glossary/sales-role.md)