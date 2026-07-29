---
title: Booking Transaction
type: entity
description: Individual completed sales booking transactions with related financial measures and dimensional links
resource: entities
tags: [booking, transaction, fact, sales, revenue]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Transaction

## Business Definition

Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions. Booking transactions represent the core revenue-generating events in the sales process.

---

## Entity Identifier

**Entity ID:** ENT008  
**Domain:** [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Table Type:** Fact Table

---

## Attributes

- **Booking ID** - Unique identifier for an individual booking transaction record
- **Order Number** - Business order number associated with the booking transaction
- **Order Line Number** - Line item number within the order associated with the booking
- **Booking Date Key** - Foreign key linking the booking transaction to the reporting date dimension
- **Customer Key** - Foreign key linking the booking transaction to the customer dimension
- **Product Key** - Foreign key linking the booking transaction to the product dimension
- **Partner Key** - Foreign key linking the booking transaction to the partner dimension
- **Geography Key** - Foreign key linking the booking transaction to the geography dimension
- **Sales Representative Key** - Foreign key linking the booking transaction to the sales representative dimension
- **Contract Key** - Foreign key linking the booking transaction to the contract dimension
- **Booking Type** - Indicates whether the booking is a new sale or a renewal
- **Renewal Indicator** - Indicates whether the booking transaction is classified as a renewal
- **Quantity Sold** - Number of units, licenses, or subscriptions included in the booking transaction
- **Unit List Price USD** - Standard list price per unit in U.S. dollars before discounts are applied
- **Discount Percentage** - Percentage discount applied to the list price for the booking transaction
- **Booking Amount USD** - Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments
- **Annual Contract Value USD** - Annualized value of the contract associated with the booking in U.S. dollars
- **Total Contract Value USD** - Total value of the full contract associated with the booking in U.S. dollars

---

## Primary Keys

- **Booking ID** (booking_id)

---

## Foreign Keys

- **Booking Date Key** (date_key) → [Date](./date.md)
- **Customer Key** (customer_key) → [Customer](./customer.md)
- **Product Key** (product_key) → [Product](./product.md)
- **Partner Key** (partner_key) → [Partner](./partner.md)
- **Geography Key** (geography_key) → [Geography](./geography.md)
- **Sales Representative Key** (sales_rep_key) → [Sales Representative](./sales-representative.md)
- **Contract Key** (contract_key) → [Contract](./contract.md)

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

---

## Measures

### Financial Measures

- **[Booking Amount USD](../measures/booking-amount-usd.md)** - Total booked revenue amount
- **[Annual Contract Value USD](../measures/annual-contract-value-usd.md)** - Annualized contract value
- **[Total Contract Value USD](../measures/total-contract-value-usd.md)** - Total contract value

### Pricing Measures

- **[Unit List Price USD](../measures/unit-list-price-usd.md)** - Standard list price per unit
- **[Discount Percentage](../measures/discount-percentage.md)** - Percentage discount applied

### Operational Measures

- **[Quantity Sold](../measures/quantity-sold.md)** - Number of units, licenses, or subscriptions

---

## Business Rules

1. Each booking transaction must have a unique Booking ID
2. Order Number and Order Line Number together identify the source order
3. All foreign keys must reference valid dimension records
4. Booking Type distinguishes new sales from renewals
5. Renewal Indicator provides binary classification of renewal status
6. Booking Amount USD represents the final revenue after discounts
7. Annual Contract Value and Total Contract Value support subscription analysis

---

## Related Concepts

- [Contract](./contract.md) - Contract terms for the booking
- [Customer](./customer.md) - Customer placing the order
- [Date](./date.md) - Date of the booking
- [Geography](./geography.md) - Geographic location of the booking
- [Partner](./partner.md) - Partner facilitating the booking
- [Product](./product.md) - Product being sold
- [Sales Representative](./sales-representative.md) - Sales representative responsible for the booking

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

## Navigation

- [Return to Entities Index](./index.md)
- [Return to Bundle Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
- [View All Relationships](../relationships/index.md)
- [View All Measures](../measures/index.md)
