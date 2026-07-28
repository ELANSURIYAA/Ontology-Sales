---
title: Booking Transaction
type: entity
description: Individual completed sales booking transactions with related financial measures and dimensional links
resource: entities
tags: [entity, fact, booking, transaction, sales, revenue]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Transaction

## Business Definition

Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions.

---

## Technical Mapping

**Source Table**: QuoteToBooking.fact_bookings

**Source System**: QuoteToBooking

**Entity Type**: Fact

---

## Attributes

- **Booking ID** (booking_id): Unique identifier for an individual booking transaction record
- **Order Number** (order_number): Business order number associated with the booking transaction
- **Order Line Number** (order_line_number): Line item number within the order associated with the booking
- **Booking Date Key** (date_key): Foreign key linking the booking transaction to the reporting date dimension
- **Customer Key** (customer_key): Foreign key linking the booking transaction to the customer dimension
- **Product Key** (product_key): Foreign key linking the booking transaction to the product dimension
- **Partner Key** (partner_key): Foreign key linking the booking transaction to the partner dimension
- **Geography Key** (geography_key): Foreign key linking the booking transaction to the geography dimension
- **Sales Representative Key** (sales_rep_key): Foreign key linking the booking transaction to the sales representative dimension
- **Contract Key** (contract_key): Foreign key linking the booking transaction to the contract dimension
- **Booking Type** (booking_type): Indicates whether the booking is a new sale or a renewal
- **Renewal Indicator** (is_renewal): Indicates whether the booking transaction is classified as a renewal
- **Quantity Sold** (quantity): Number of units, licenses, or subscriptions included in the booking transaction
- **Unit List Price USD** (unit_list_price_usd): Standard list price per unit in U.S. dollars before discounts are applied
- **Discount Percentage** (discount_pct): Percentage discount applied to the list price for the booking transaction
- **Booking Amount USD** (booking_amount_usd): Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments
- **Annual Contract Value USD** (acv_usd): Annualized value of the contract associated with the booking in U.S. dollars
- **Total Contract Value USD** (tcv_usd): Total value of the full contract associated with the booking in U.S. dollars

---

## Primary Keys

- **Booking ID** (booking_id)
- **Order Number** (order_number)
- **Order Line Number** (order_line_number)

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

- **[Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)**: One-to-Many relationship from Contract
- **[Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)**: One-to-Many relationship from Customer
- **[Date to Booking Transaction](../relationships/date-to-booking-transaction.md)**: One-to-Many relationship from Date
- **[Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)**: One-to-Many relationship from Geography
- **[Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)**: One-to-Many relationship from Partner
- **[Product to Booking Transaction](../relationships/product-to-booking-transaction.md)**: One-to-Many relationship from Product
- **[Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)**: One-to-Many relationship from Sales Representative

### Related Entities

- [Contract](contract.md): Dimension entity referenced by this fact
- [Customer](customer.md): Dimension entity referenced by this fact
- [Date](date.md): Dimension entity referenced by this fact
- [Geography](geography.md): Dimension entity referenced by this fact
- [Partner](partner.md): Dimension entity referenced by this fact
- [Product](product.md): Dimension entity referenced by this fact
- [Sales Representative](sales-representative.md): Dimension entity referenced by this fact

---

## Measures

This fact entity contains the following measures:

- **[Quantity Sold](../measures/quantity-sold.md)**: Number of units, licenses, or subscriptions (SUM)
- **[Unit List Price USD](../measures/unit-list-price-usd.md)**: Standard list price per unit before discounts (SUM)
- **[Discount Percentage](../measures/discount-percentage.md)**: Percentage discount applied to list price (AVG)
- **[Booking Amount USD](../measures/booking-amount-usd.md)**: Total booked revenue after pricing adjustments (SUM)
- **[Annual Contract Value USD](../measures/annual-contract-value-usd.md)**: Annualized value of the contract (SUM)
- **[Total Contract Value USD](../measures/total-contract-value-usd.md)**: Total value of the full contract (SUM)

---

## Related Concepts

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

## Business Rules

1. Booking ID is the unique identifier for each booking transaction
2. Order Number and Order Line Number together identify the source order line
3. Every booking transaction must reference valid dimension records
4. Booking Type classifies transactions as new sales or renewals
5. Renewal Indicator provides a binary flag for renewal classification
6. Quantity Sold represents the number of units, licenses, or subscriptions
7. Unit List Price USD is the standard price before discounts
8. Discount Percentage is applied to calculate the final booking amount
9. Booking Amount USD is the primary revenue metric
10. Annual Contract Value (ACV) represents annualized contract value
11. Total Contract Value (TCV) represents full contract commitment
12. All financial measures are recorded in U.S. dollars
13. Booking transactions are immutable once recorded
14. Each transaction must have a booking date

---

## Usage Examples

**Revenue Analysis**:
- Calculate total booking revenue by fiscal period
- Analyze booking trends over time
- Compare actual bookings to targets

**Customer Analysis**:
- Measure booking revenue by customer segment
- Analyze customer purchase patterns
- Identify top customers by booking amount

**Product Analysis**:
- Evaluate product performance by booking revenue
- Analyze product mix and portfolio balance
- Compare product family contributions

**Geographic Analysis**:
- Measure booking performance by sales region
- Analyze geographic distribution of revenue
- Compare theater and country performance

**Partner Analysis**:
- Evaluate partner contribution to bookings
- Analyze channel performance
- Compare direct vs. indirect sales

**Sales Performance**:
- Measure sales representative productivity
- Analyze team performance
- Track quota attainment

**Contract Analysis**:
- Analyze ACV and TCV by contract type
- Measure renewal rates
- Evaluate contract term preferences

**Pricing Analysis**:
- Analyze discount rates by dimension
- Measure price realization
- Evaluate pricing strategy effectiveness

---

## Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Main Index](../index.md)
- [View Relationships](../relationships/index.md)
- [View Measures](../measures/index.md)
- [View Glossary](../glossary/index.md)
