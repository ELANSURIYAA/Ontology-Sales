---
title: Booking Transaction
type: entity
description: Business entity representing individual completed sales booking transactions with financial measures
resource: entities
tags: [entity, fact, booking, transaction, sales, revenue]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Transaction

## Business Definition

Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions. The Booking Transaction entity serves as the central fact table for sales booking analysis and revenue reporting.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: fact_bookings  
**Entity Type**: Fact  
**Entity ID**: ENT008

---

## Attributes

- **Booking ID** (booking_id) - integer, NOT NULL
- **Order Number** (order_number) - character varying(20), NULL
- **Order Line Number** (order_line_number) - integer, NULL
- **Booking Date Key** (date_key) - integer, NULL
- **Customer Key** (customer_key) - integer, NULL
- **Product Key** (product_key) - integer, NULL
- **Partner Key** (partner_key) - integer, NULL
- **Geography Key** (geography_key) - integer, NULL
- **Sales Representative Key** (sales_rep_key) - integer, NULL
- **Contract Key** (contract_key) - integer, NULL
- **Booking Type** (booking_type) - character varying(15), NULL
- **Renewal Indicator** (is_renewal) - integer, NULL
- **Quantity Sold** (quantity) - integer, NULL
- **Unit List Price USD** (unit_list_price_usd) - numeric, NULL
- **Discount Percentage** (discount_pct) - numeric, NULL
- **Booking Amount USD** (booking_amount_usd) - numeric, NULL
- **Annual Contract Value USD** (acv_usd) - numeric, NULL
- **Total Contract Value USD** (tcv_usd) - numeric, NULL

---

## Primary Keys

- **Booking ID** (booking_id)

---

## Foreign Keys

- **Booking Date Key** (date_key) → [Date](date.md)
- **Customer Key** (customer_key) → [Customer](customer.md)
- **Product Key** (product_key) → [Product](product.md)
- **Partner Key** (partner_key) → [Partner](partner.md)
- **Geography Key** (geography_key) → [Geography](geography.md)
- **Sales Representative Key** (sales_rep_key) → [Sales Representative](sales-representative.md)
- **Contract Key** (contract_key) → [Contract](contract.md)

---

## Relationships

### Incoming Relationships

- [Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md) - Links from Contract dimension (Many-to-One)
- [Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md) - Links from Customer dimension (Many-to-One)
- [Date to Booking Transaction](../relationships/date-to-booking-transaction.md) - Links from Date dimension (Many-to-One)
- [Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md) - Links from Geography dimension (Many-to-One)
- [Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md) - Links from Partner dimension (Many-to-One)
- [Product to Booking Transaction](../relationships/product-to-booking-transaction.md) - Links from Product dimension (Many-to-One)
- [Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md) - Links from Sales Representative dimension (Many-to-One)

---

## Measures

### Volume Measures
- [Quantity Sold](../measures/quantity-sold.md) - Number of units, licenses, or subscriptions sold

### Pricing Measures
- [Unit List Price USD](../measures/unit-list-price-usd.md) - Standard list price per unit before discounts
- [Discount Percentage](../measures/discount-percentage.md) - Percentage discount applied to list price

### Revenue Measures
- [Booking Amount USD](../measures/booking-amount-usd.md) - Total booked revenue after pricing adjustments
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md) - Annualized contract value
- [Total Contract Value USD](../measures/total-contract-value-usd.md) - Total contract value over full term

---

## Related Concepts

### Related Entities
- [Contract](contract.md) - Contract associated with the booking
- [Customer](customer.md) - Customer placing the booking
- [Date](date.md) - Date of the booking transaction
- [Geography](geography.md) - Geographic location of the booking
- [Partner](partner.md) - Partner involved in the booking
- [Product](product.md) - Product sold in the booking
- [Sales Representative](sales-representative.md) - Sales representative managing the booking

### Related Glossary Terms
- [Booking Transaction](../glossary/booking-transaction.md)
- [Booking ID](../glossary/booking-id.md)
- [Order Number](../glossary/order-number.md)
- [Order Line Number](../glossary/order-line-number.md)
- [Booking Date Key](../glossary/booking-date-key.md)
- [Booking Type](../glossary/booking-type.md)
- [Renewal Indicator](../glossary/renewal-indicator.md)
- [Quantity Sold](../glossary/quantity-sold.md)
- [Unit List Price USD](../glossary/unit-list-price-usd.md)
- [Discount Percentage](../glossary/discount-percentage.md)
- [Booking Amount USD](../glossary/booking-amount-usd.md)
- [Annual Contract Value USD](../glossary/annual-contract-value-usd.md)
- [Total Contract Value USD](../glossary/total-contract-value-usd.md)

### Related Domains
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Uniqueness**: Each booking transaction is uniquely identified by Booking ID
2. **Business Keys**: Order Number and Order Line Number provide business-level identification
3. **Dimensional Links**: Every booking transaction links to exactly one record in each dimension table
4. **Booking Types**: Booking Type indicates whether the transaction is a new sale or renewal
5. **Renewal Classification**: Renewal Indicator (is_renewal) provides binary classification of renewal transactions
6. **Revenue Calculation**: Booking Amount = Quantity × Unit List Price × (1 - Discount Percentage)
7. **Contract Values**: ACV and TCV represent annualized and total contract values respectively
8. **Data Completeness**: All foreign keys should reference valid dimension records

---

## Usage Examples

### Total Revenue Analysis
Sum Booking Amount USD across all dimensions to calculate total revenue for any time period or dimension slice.

### New vs Renewal Analysis
Compare booking amounts for new sales (Booking Type = 'New') versus renewals (Booking Type = 'Renewal').

### Average Deal Size
Calculate average booking amount by dividing total Booking Amount USD by count of distinct Booking IDs.

### Discount Analysis
Analyze average Discount Percentage by customer segment, partner type, or sales representative.

### Contract Value Analysis
Compare Annual Contract Value and Total Contract Value across customer segments and product families.

---

## Data Quality Notes

- Booking ID is mandatory and serves as the primary key
- All foreign keys should reference valid dimension records
- Measure values (quantities, amounts, percentages) should be validated for reasonableness
- Booking Amount should align with calculated value from quantity, price, and discount
- Booking Type and Renewal Indicator should be consistent
- NULL values in foreign keys indicate missing dimensional context
- Date Key should always be populated for time-based analysis

---

## Navigation

- [View Entity Index](index.md)
- [View Related Relationships](../relationships/index.md)
- [View Related Measures](../measures/index.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Entity ID**: ENT008  
**Domain**: Sales Bookings and Revenue Analytics  
**Entity Type**: Fact  
**Attribute Count**: 18  
**Relationship Count**: 7  
**Measure Count**: 6  
**Last Updated**: 2026-07-28T00:00:00Z
