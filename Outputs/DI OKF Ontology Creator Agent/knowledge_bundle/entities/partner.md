---
title: Partner
type: entity
id: ENT005
domain: Sales Bookings and Revenue Analytics
technical_table: QuoteToBooking.dim_partner
business_keys:
  - partner_key
  - partner_id
version: 1.0
status: generated
---

# Partner

## Business Definition

Stores partner master data used to analyze indirect and direct sales activity by partner identity, partner type, tier, and route to market.

## Technical Mapping

- Table: `QuoteToBooking.dim_partner`
- Primary business key(s): `partner_key`, `partner_id`

## Attributes

| Attribute | Technical Column | Data Type | Nullable | PK | FK | Description |
| --- | --- | --- | --- | --- | --- | --- |
| Partner Key | partner_key | integer | No | Yes | No | Surrogate key that uniquely identifies a partner record in the partner dimension. |
| Partner ID | partner_id | character varying | No | No | No | Business identifier assigned to the partner organization. |
| Partner Name | partner_name | character varying | Yes | No | No | Name of the partner organization involved in the sale or fulfillment process. |
| Partner Type | partner_type | character varying | Yes | No | No | Classifies the partner by business role, such as distributor, reseller, systems integrator, or direct. |
| Partner Tier | partner_tier | character varying | Yes | No | No | Indicates the partner’s program tier or accreditation level. |
| Route to Market | route_to_market | character varying | Yes | No | No | Describes the sales channel path through which the offering reaches the customer. |

## Keys

- Primary Key: `partner_key`
- Alternate Business Key: `partner_id`
- Referenced by: [Booking Transaction](booking-transaction.md)

## Measures

- No direct measures defined for this entity.

## Relationships

- Parent in [Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)

## Related Concepts

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Booking Transaction](booking-transaction.md)
- [Partner](../glossary/partner.md)
- [Route to Market](../glossary/route-to-market.md)