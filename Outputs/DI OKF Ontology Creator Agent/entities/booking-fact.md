---
title: Booking Fact
type: entity
description: Individual booking transactions and financial measures for analyzing sales performance
resource: entities
tags: [okf, entity, booking, fact, sales-transactions]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Fact

## Business Definition

The Booking Fact stores individual booking transactions and their financial measures for analyzing sales performance across customers, products, partners, geographies, contracts, sales representatives, and time. This is the central fact table in the star schema containing all transactional booking data and measures.

---

## Technical Mapping

**Source Schema**: quotetobooking  
**Source Table**: fact_bookings  
**Entity Type**: Fact  
**Grain**: Individual booking transaction line (one record per order line)

---

## Attributes

- booking_id
- order_number
- order_line_number
- date_key
- customer_key
- product_key
- partner_key
- geography_key
- sales_rep_key
- contract_key
- booking_type
- is_renewal
- quantity
- unit_list_price_usd
- discount_pct
- booking_amount_usd
- acv_usd
- tcv_usd

---

## Primary Keys

- booking_id

---

## Foreign Keys

- date_key (references Date Dimension)
- customer_key (references Customer Dimension)
- product_key (references Product Dimension)
- partner_key (references Partner Dimension)
- geography_key (references Geography Dimension)
- sales_rep_key (references Sales Representative Dimension)
- contract_key (references Contract Dimension)

---

## Relationships

### Inbound Relationships
- [Contract to Booking](../relationships/contract-to-booking.md) - Many-to-One relationship from Contract Dimension
- [Customer to Booking](../relationships/customer-to-booking.md) - Many-to-One relationship from Customer Dimension
- [Date to Booking](../relationships/date-to-booking.md) - Many-to-One relationship from Date Dimension
- [Geography to Booking](../relationships/geography-to-booking.md) - Many-to-One relationship from Geography Dimension
- [Partner to Booking](../relationships/partner-to-booking.md) - Many-to-One relationship from Partner Dimension
- [Product to Booking](../relationships/product-to-booking.md) - Many-to-One relationship from Product Dimension
- [Sales Representative to Booking](../relationships/sales-representative-to-booking.md) - Many-to-One relationship from Sales Representative Dimension

---

## Measures

- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Related Concepts

### Related Entities
- [Contract Dimension](contract-dimension.md)
- [Customer Dimension](customer-dimension.md)
- [Date Dimension](date-dimension.md)
- [Geography Dimension](geography-dimension.md)
- [Partner Dimension](partner-dimension.md)
- [Product Dimension](product-dimension.md)
- [Sales Representative Dimension](sales-representative-dimension.md)

### Related Domains
- [Sales Transactions](../domains/sales-transactions.md)
- [Revenue Metrics](../domains/revenue-metrics.md)
- [Pricing](../domains/pricing.md)

### Related Glossary Terms
- [Booking Fact](../glossary/booking-fact.md)
- [Booking ID](../glossary/booking-id.md)
- [Order Number](../glossary/order-number.md)
- [Order Line Number](../glossary/order-line-number.md)
- [Booking Type](../glossary/booking-type.md)
- [Renewal Indicator](../glossary/renewal-indicator.md)
- [Quantity Sold](../glossary/quantity-sold.md)
- [Unit List Price USD](../glossary/unit-list-price-usd.md)
- [Discount Percentage](../glossary/discount-percentage.md)
- [Booking Amount USD](../glossary/booking-amount-usd.md)
- [Annual Contract Value USD](../glossary/annual-contract-value-usd.md)
- [Total Contract Value USD](../glossary/total-contract-value-usd.md)

---

## Business Rules

1. Booking ID must be unique and not null
2. All foreign keys must reference valid dimension records
3. Quantity must be greater than zero
4. Booking Amount must be non-negative
5. Total Contract Value must be greater than or equal to Annual Contract Value
6. Renewal Indicator must align with Booking Type classification
7. Discount Percentage must be between 0 and 100
8. Order Number and Order Line Number combination should be unique

---

## Attribute Details

### booking_id
- **Data Type**: integer
- **Nullable**: No
- **Primary Key**: Yes
- **Description**: Unique identifier for an individual booking transaction

### order_number
- **Data Type**: character varying(20)
- **Nullable**: Yes
- **Description**: Sales order number associated with the booking transaction

### order_line_number
- **Data Type**: integer
- **Nullable**: Yes
- **Description**: Line number within the sales order that identifies the specific booked item

### date_key
- **Data Type**: integer
- **Nullable**: Yes
- **Foreign Key**: Yes
- **Description**: Reference to the date dimension indicating when the booking was recorded

### customer_key
- **Data Type**: integer
- **Nullable**: Yes
- **Foreign Key**: Yes
- **Description**: Reference to the customer associated with the booking

### product_key
- **Data Type**: integer
- **Nullable**: Yes
- **Foreign Key**: Yes
- **Description**: Reference to the product or offer included in the booking

### partner_key
- **Data Type**: integer
- **Nullable**: Yes
- **Foreign Key**: Yes
- **Description**: Reference to the partner involved in fulfilling or transacting the booking

### geography_key
- **Data Type**: integer
- **Nullable**: Yes
- **Foreign Key**: Yes
- **Description**: Reference to the geography associated with the booking

### sales_rep_key
- **Data Type**: integer
- **Nullable**: Yes
- **Foreign Key**: Yes
- **Description**: Reference to the sales representative responsible for the booking

### contract_key
- **Data Type**: integer
- **Nullable**: Yes
- **Foreign Key**: Yes
- **Description**: Reference to the contract or commercial agreement associated with the booking

### booking_type
- **Data Type**: character varying(15)
- **Nullable**: Yes
- **Description**: Classification of the booking event, such as new business or renewal

### is_renewal
- **Data Type**: integer
- **Nullable**: Yes
- **Description**: Indicator showing whether the booking represents a renewal transaction

### quantity
- **Data Type**: integer
- **Nullable**: Yes
- **Description**: Number of units, licenses, or subscriptions booked in the transaction

### unit_list_price_usd
- **Data Type**: numeric(12,2)
- **Nullable**: Yes
- **Description**: Standard list price per unit in U.S. dollars before discounts

### discount_pct
- **Data Type**: numeric(5,2)
- **Nullable**: Yes
- **Description**: Discount applied to the list price for the booking line

### booking_amount_usd
- **Data Type**: numeric(14,2)
- **Nullable**: Yes
- **Description**: Total booked revenue amount in U.S. dollars for the transaction

### acv_usd
- **Data Type**: numeric(14,2)
- **Nullable**: Yes
- **Description**: Annualized contract value in U.S. dollars used for recurring revenue analysis

### tcv_usd
- **Data Type**: numeric(14,2)
- **Nullable**: Yes
- **Description**: Total contract value in U.S. dollars over the full contract term

---

## Analytical Use Cases

- Track booking revenue across all dimensions
- Analyze sales performance trends over time
- Measure new business versus renewal activity
- Monitor pricing and discount effectiveness
- Calculate contract values and recurring revenue
- Evaluate sales representative and team performance
- Assess product, customer, and partner contribution

---

## Data Quality Metrics

- **Completeness**: Booking ID and all foreign keys must be 100% populated
- **Uniqueness**: Booking ID must be unique
- **Validity**: All foreign keys must reference valid dimension records
- **Consistency**: Revenue measures must follow logical relationships (TCV ≥ ACV)

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Bundle Index](../index.md)
