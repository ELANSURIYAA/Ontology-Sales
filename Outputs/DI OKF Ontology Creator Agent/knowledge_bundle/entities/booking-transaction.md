---
title: Booking Transaction
type: entity
id: ENT008
domain: Sales Bookings and Revenue Analytics
technical_table: QuoteToBooking.fact_bookings
business_keys:
  - booking_id
  - order_number
  - order_line_number
version: 1.0
status: generated
---

# Booking Transaction

## Business Definition

Stores individual completed sales booking transactions and their associated financial measures, linked to customer, product, partner, geography, sales representative, contract, and date dimensions.

## Technical Mapping

- Table: `QuoteToBooking.fact_bookings`
- Primary business key(s): `booking_id`, `order_number`, `order_line_number`

## Attributes

| Attribute | Technical Column | Data Type | Nullable | PK | FK | Description |
| --- | --- | --- | --- | --- | --- | --- |
| Booking ID | booking_id | integer | No | Yes | No | Unique identifier for the booking transaction record. |
| Order Number | order_number | character varying | Yes | No | No | Business order number associated with the booking transaction. |
| Order Line Number | order_line_number | integer | Yes | No | No | Line number within the order associated with the booking transaction. |
| Booking Date Key | date_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the date dimension. |
| Customer Key | customer_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the customer dimension. |
| Product Key | product_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the product dimension. |
| Partner Key | partner_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the partner dimension. |
| Geography Key | geography_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the geography dimension. |
| Sales Representative Key | sales_rep_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the sales representative dimension. |
| Contract Key | contract_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the contract dimension. |
| Booking Type | booking_type | character varying | Yes | No | No | Indicates whether the booking is a new sale or a renewal. |
| Renewal Indicator | is_renewal | integer | Yes | No | No | Indicates whether the booking transaction represents a renewal event. |
| Quantity Sold | quantity | integer | Yes | No | No | Number of units, licenses, or service quantities included in the booking. |
| Unit List Price USD | unit_list_price_usd | numeric | Yes | No | No | Standard list price per unit in U.S. dollars before discounts. |
| Discount Percentage | discount_pct | numeric | Yes | No | No | Discount applied to the list price for the booking transaction. |
| Booking Amount USD | booking_amount_usd | numeric | Yes | No | No | Total booked sales value recognized for the transaction in U.S. dollars. |
| Annual Contract Value USD | acv_usd | numeric | Yes | No | No | Annualized value of the contract associated with the booking in U.S. dollars. |
| Total Contract Value USD | tcv_usd | numeric | Yes | No | No | Total contract value associated with the booking in U.S. dollars over the contract term. |

## Keys

- Primary Key: `booking_id`
- Alternate Business Keys: `order_number`, `order_line_number`
- Foreign Keys: `date_key`, `customer_key`, `product_key`, `partner_key`, `geography_key`, `sales_rep_key`, `contract_key`

## Measures

- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

## Relationships

- Child in [Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)
- Child in [Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)
- Child in [Date to Booking Transaction](../relationships/date-to-booking-transaction.md)
- Child in [Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)
- Child in [Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)
- Child in [Product to Booking Transaction](../relationships/product-to-booking-transaction.md)
- Child in [Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)

## Related Concepts

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Contract](contract.md)
- [Customer](customer.md)
- [Date](date.md)
- [Geography](geography.md)
- [Partner](partner.md)
- [Product](product.md)
- [Sales Representative](sales-representative.md)
- [Booking Transaction](../glossary/booking-transaction.md)