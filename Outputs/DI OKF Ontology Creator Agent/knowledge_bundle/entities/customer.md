---
title: Customer
type: entity
id: ENT002
domain: Sales Bookings and Revenue Analytics
technical_table: QuoteToBooking.dim_customer
business_keys:
  - customer_key
  - customer_id
version: 1.0
status: generated
---

# Customer

## Business Definition

Stores customer master data used to analyze bookings by customer identity, market segment, industry, account tier, and headquarters location.

## Technical Mapping

- Table: `QuoteToBooking.dim_customer`
- Primary business key(s): `customer_key`, `customer_id`

## Attributes

| Attribute | Technical Column | Data Type | Nullable | PK | FK | Description |
| --- | --- | --- | --- | --- | --- | --- |
| Customer Key | customer_key | integer | No | Yes | No | Surrogate key that uniquely identifies a customer record in the customer dimension. |
| Customer ID | customer_id | character varying | No | No | No | Business identifier assigned to the customer account. |
| Customer Name | customer_name | character varying | Yes | No | No | Name of the customer organization associated with the booking. |
| Customer Segment | segment | character varying | Yes | No | No | Classifies the customer into a business segment such as Enterprise, Service Provider, or Public Sector. |
| Industry | industry | character varying | Yes | No | No | Indicates the customer’s industry classification for business analysis. |
| Account Tier | account_tier | character varying | Yes | No | No | Identifies the strategic importance or service tier of the customer account. |
| Headquarters Country | hq_country | character varying | Yes | No | No | Country where the customer’s headquarters is located. |
| Headquarters Region | hq_region | character varying | Yes | No | No | Region where the customer’s headquarters is located, such as Americas, EMEA, or APJC. |

## Keys

- Primary Key: `customer_key`
- Alternate Business Key: `customer_id`
- Referenced by: [Booking Transaction](booking-transaction.md)

## Measures

- No direct measures defined for this entity.

## Relationships

- Parent in [Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)

## Related Concepts

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Booking Transaction](booking-transaction.md)
- [Customer](../glossary/customer.md)
- [Customer Segment](../glossary/customer-segment.md)