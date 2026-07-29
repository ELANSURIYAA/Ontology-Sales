---
title: Booking Transaction
type: entity
description: Individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions
resource: entities
tags: [booking, transaction, fact, sales, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Transaction

## Business Definition

The Booking Transaction entity stores individual completed sales booking transactions with related financial measures and dimensional context. It serves as the central fact entity in the sales bookings model, linking to seven dimension entities (Contract, Customer, Date, Geography, Partner, Product, Sales Representative) and containing six financial measures. This entity enables comprehensive analysis of sales performance across all business dimensions.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings  
**Source Schema**: QuoteToBooking  
**Entity Type**: Fact  
**Entity ID**: ENT008

---

## Attributes

### Business Keys
- **Booking ID** - Unique identifier for an individual booking transaction record
- **Order Number** - Business order number associated with the booking transaction
- **Order Line Number** - Line item number within the order associated with the booking

### Foreign Keys
- **Booking Date Key** - Foreign key linking the booking transaction to the reporting date dimension
- **Customer Key** - Foreign key linking the booking transaction to the customer dimension
- **Product Key** - Foreign key linking the booking transaction to the product dimension
- **Partner Key** - Foreign key linking the booking transaction to the partner dimension
- **Geography Key** - Foreign key linking the booking transaction to the geography dimension
- **Sales Representative Key** - Foreign key linking the booking transaction to the sales representative dimension
- **Contract Key** - Foreign key linking the booking transaction to the contract dimension

### Descriptive Attributes
- **Booking Type** - Indicates whether the booking is a new sale or a renewal
- **Renewal Indicator** - Indicates whether the booking transaction is classified as a renewal

### Measure Attributes
- **Quantity Sold** - Number of units, licenses, or subscriptions included in the booking transaction
- **Unit List Price USD** - Standard list price per unit in U.S. dollars before discounts are applied
- **Discount Percentage** - Percentage discount applied to the list price for the booking transaction
- **Booking Amount USD** - Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments
- **Annual Contract Value USD** - Annualized value of the contract associated with the booking in U.S. dollars
- **Total Contract Value USD** - Total value of the full contract associated with the booking in U.S. dollars

---

## Primary Keys

- **Booking ID** (booking_id) - Integer, Not Nullable
- **Order Number** (order_number) - Character Varying(20), Nullable
- **Order Line Number** (order_line_number) - Integer, Nullable

---

## Foreign Keys

| Foreign Key | References | Relationship |
|-------------|------------|--------------|
| date_key | [Date](./date.md) | Many-to-One |
| customer_key | [Customer](./customer.md) | Many-to-One |
| product_key | [Product](./product.md) | Many-to-One |
| partner_key | [Partner](./partner.md) | Many-to-One |
| geography_key | [Geography](./geography.md) | Many-to-One |
| sales_rep_key | [Sales Representative](./sales-representative.md) | Many-to-One |
| contract_key | [Contract](./contract.md) | Many-to-One |

---

## Relationships

### Incoming Relationships

- **[Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)** - Links from Contract dimension
- **[Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)** - Links from Customer dimension
- **[Date to Booking Transaction](../relationships/date-to-booking-transaction.md)** - Links from Date dimension
- **[Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)** - Links from Geography dimension
- **[Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)** - Links from Partner dimension
- **[Product to Booking Transaction](../relationships/product-to-booking-transaction.md)** - Links from Product dimension
- **[Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)** - Links from Sales Representative dimension

### Related Entities

- **[Contract](./contract.md)** - Contract terms and conditions
- **[Customer](./customer.md)** - Customer placing the order
- **[Date](./date.md)** - Booking date and fiscal period
- **[Geography](./geography.md)** - Geographic location of booking
- **[Partner](./partner.md)** - Partner involved in transaction
- **[Product](./product.md)** - Product or service sold
- **[Sales Representative](./sales-representative.md)** - Sales personnel credited

---

## Measures

### Volume Measures
- **[Quantity Sold](../measures/quantity-sold.md)** - Units, licenses, or subscriptions sold

### Pricing Measures
- **[Unit List Price USD](../measures/unit-list-price-usd.md)** - Standard list price per unit
- **[Discount Percentage](../measures/discount-percentage.md)** - Price discount percentage

### Revenue Measures
- **[Booking Amount USD](../measures/booking-amount-usd.md)** - Total booked revenue
- **[Annual Contract Value USD](../measures/annual-contract-value-usd.md)** - Annualized contract value
- **[Total Contract Value USD](../measures/total-contract-value-usd.md)** - Total contract value

---

## Business Rules

### Data Quality Rules
1. Booking ID must be unique and not null
2. Every booking must reference a valid customer
3. Every booking must reference a valid product
4. Every booking must reference a valid date
5. All foreign keys must reference existing dimension records
6. Booking Amount must be non-negative
7. Quantity Sold must be positive
8. Discount Percentage must be between 0 and 100

### Business Logic Rules
1. Booking Amount = Quantity × Unit List Price × (1 - Discount Percentage / 100)
2. Annual Contract Value (ACV) = Total Contract Value ÷ Contract Term (Years)
3. Renewal bookings must have Renewal Indicator = 1
4. New bookings must have Booking Type = 'New'
5. Renewal bookings must have Booking Type = 'Renewal'

### Referential Integrity Rules
1. date_key must exist in Date dimension
2. customer_key must exist in Customer dimension
3. product_key must exist in Product dimension
4. partner_key must exist in Partner dimension
5. geography_key must exist in Geography dimension
6. sales_rep_key must exist in Sales Representative dimension
7. contract_key must exist in Contract dimension

---

## Analytical Usage

### Dimensional Analysis

Booking transactions can be analyzed across all dimensions:

- **Time Analysis** - Trends by calendar and fiscal periods
- **Customer Analysis** - Performance by segment, industry, tier
- **Product Analysis** - Portfolio performance by family and domain
- **Geographic Analysis** - Regional and country performance
- **Partner Analysis** - Channel and partner contribution
- **Contract Analysis** - Contract type and term analysis
- **Sales Analysis** - Representative and team performance

### Measure Analysis

- **Revenue Analysis** - Booking amounts, ACV, and TCV
- **Volume Analysis** - Quantity and unit analysis
- **Pricing Analysis** - List price and discount effectiveness
- **Growth Analysis** - Period-over-period comparisons
- **Mix Analysis** - Product, customer, and channel mix

### Aggregation Patterns

- **Sum**: Quantity, Booking Amount, ACV, TCV, Unit List Price
- **Average**: Discount Percentage, Unit List Price
- **Count**: Number of bookings, Number of orders
- **Distinct Count**: Unique customers, Unique products

---

## Related Concepts

All dimension entities are related to Booking Transaction:

- **[Contract](./contract.md)** - Contract terms
- **[Customer](./customer.md)** - Purchasing customer
- **[Date](./date.md)** - Transaction date
- **[Geography](./geography.md)** - Transaction location
- **[Partner](./partner.md)** - Channel partner
- **[Product](./product.md)** - Product sold
- **[Sales Representative](./sales-representative.md)** - Sales credit

---

## Glossary Terms

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

---

## Attribute Details

| Attribute | Technical Column | Data Type | Nullable | Key Type | Description |
|-----------|-----------------|-----------|----------|----------|-------------|
| Booking ID | booking_id | integer | No | Primary | Unique identifier for booking transaction |
| Order Number | order_number | character varying(20) | Yes | Business | Business order number |
| Order Line Number | order_line_number | integer | Yes | Business | Order line item number |
| Booking Date Key | date_key | integer | Yes | Foreign | Link to date dimension |
| Customer Key | customer_key | integer | Yes | Foreign | Link to customer dimension |
| Product Key | product_key | integer | Yes | Foreign | Link to product dimension |
| Partner Key | partner_key | integer | Yes | Foreign | Link to partner dimension |
| Geography Key | geography_key | integer | Yes | Foreign | Link to geography dimension |
| Sales Representative Key | sales_rep_key | integer | Yes | Foreign | Link to sales representative dimension |
| Contract Key | contract_key | integer | Yes | Foreign | Link to contract dimension |
| Booking Type | booking_type | character varying(15) | Yes | - | New or renewal classification |
| Renewal Indicator | is_renewal | integer | Yes | - | Renewal flag (0 or 1) |
| Quantity Sold | quantity | integer | Yes | Measure | Number of units sold |
| Unit List Price USD | unit_list_price_usd | numeric | Yes | Measure | Standard list price per unit |
| Discount Percentage | discount_pct | numeric | Yes | Measure | Discount percentage applied |
| Booking Amount USD | booking_amount_usd | numeric | Yes | Measure | Total booked revenue |
| Annual Contract Value USD | acv_usd | numeric | Yes | Measure | Annualized contract value |
| Total Contract Value USD | tcv_usd | numeric | Yes | Measure | Total contract value |

---

## Semantic Links

- [Entity Index](./index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Relationship Index](../relationships/index.md)
- [Measure Index](../measures/index.md)
- [Main Index](../index.md)

---

## Metadata

**Entity ID**: ENT008  
**Domain ID**: DOM001  
**Entity Type**: Fact  
**Technical Table**: QuoteToBooking.fact_bookings  
**Total Attributes**: 18  
**Total Foreign Keys**: 7  
**Total Measures**: 6  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
