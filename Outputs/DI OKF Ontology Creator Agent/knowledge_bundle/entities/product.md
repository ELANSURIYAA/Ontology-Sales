---
title: Product
type: entity
id: ENT006
domain: Sales Bookings and Revenue Analytics
technical_table: QuoteToBooking.dim_product
business_keys:
  - product_key
  - product_id
version: 1.0
status: generated
---

# Product

## Business Definition

Stores product master data used to analyze bookings by product identity, family, technology domain, offer type, and business entity.

## Technical Mapping

- Table: `QuoteToBooking.dim_product`
- Primary business key(s): `product_key`, `product_id`

## Attributes

| Attribute | Technical Column | Data Type | Nullable | PK | FK | Description |
| --- | --- | --- | --- | --- | --- | --- |
| Product Key | product_key | integer | No | Yes | No | Surrogate key that uniquely identifies a product record in the product dimension. |
| Product ID | product_id | character varying | No | No | No | Business identifier or SKU assigned to the product or offering. |
| Product Name | product_name | character varying | Yes | No | No | Name of the product, solution, or subscription offering. |
| Product Family | product_family | character varying | Yes | No | No | Groups related products into a common family for portfolio analysis. |
| Technology Domain | technology_domain | character varying | Yes | No | No | Identifies the technology area associated with the product, such as networking, security, or collaboration. |
| Offer Type | offer_type | character varying | Yes | No | No | Indicates whether the offering is hardware, software subscription, or SaaS subscription. |
| Business Entity | business_entity | character varying | Yes | No | No | Identifies the internal business unit or portfolio associated with the product. |

## Keys

- Primary Key: `product_key`
- Alternate Business Key: `product_id`
- Referenced by: [Booking Transaction](booking-transaction.md)

## Measures

- No direct measures defined for this entity.

## Relationships

- Parent in [Product to Booking Transaction](../relationships/product-to-booking-transaction.md)

## Related Concepts

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Booking Transaction](booking-transaction.md)
- [Product](../glossary/product.md)
- [Technology Domain](../glossary/technology-domain.md)