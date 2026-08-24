---
title: Bookings
type: entity
description: Captures individual completed sales booking transactions and their associated financial measures, quantities, renewal status, and links to related business dimensions
resource: entities
tags: [bookings, fact-table, transactions, sales, revenue]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings

## Business Definition

The Bookings entity represents the core fact table that captures individual completed sales booking transactions. Each record represents a single booking transaction at the order line level, containing financial measures (booking amount, ACV, TCV), quantities, pricing information, renewal status, and foreign key references to related dimensional entities such as customers, products, partners, geographies, sales representatives, contracts, and dates.

This entity serves as the foundation for all sales booking and revenue analytics, enabling comprehensive analysis of sales performance across multiple business dimensions.

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings

**Source Schema**: quotetobooking

**Entity Type**: Fact Table

**Grain**: Booking transaction (order line level)

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

- date_key → [Dates](./dates.md)
- customer_key → [Customers](./customers.md)
- product_key → [Products](./products.md)
- partner_key → [Partners](./partners.md)
- geography_key → [Geographies](./geographies.md)
- sales_rep_key → [Sales Representatives](./sales-representatives.md)
- contract_key → [Contracts](./contracts.md)

---

## Relationships

- [Bookings to Contracts](../relationships/bookings-to-contracts.md)
- [Bookings to Customers](../relationships/bookings-to-customers.md)
- [Bookings to Dates](../relationships/bookings-to-dates.md)
- [Bookings to Geographies](../relationships/bookings-to-geographies.md)
- [Bookings to Partners](../relationships/bookings-to-partners.md)
- [Bookings to Products](../relationships/bookings-to-products.md)
- [Bookings to Sales Representatives](../relationships/bookings-to-sales-representatives.md)

---

## Measures

- [Booking Count](../measures/booking-count.md)
- [Distinct Order Count](../measures/distinct-order-count.md)
- [Total Quantity](../measures/total-quantity.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Average Discount Percentage](../measures/average-discount-pct.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

---

## Related Concepts

- [Booking Transaction](../glossary/booking-transaction.md)
- [Annual Contract Value](../glossary/annual-contract-value.md)
- [Total Contract Value](../glossary/total-contract-value.md)
- [Renewal](../glossary/renewal.md)
- [Net New Business](../glossary/net-new-business.md)
- [Booking Amount](../glossary/booking-amount.md)
- [Discount Percentage](../glossary/discount-percentage.md)
- [Sales Order](../glossary/sales-order.md)

---

## Business Rules

1. **Unique Booking Identifier**: Each booking transaction must have a unique booking_id
2. **Order Line Grain**: Each record represents a single line item within a sales order
3. **Foreign Key Integrity**: All foreign keys must reference valid dimension records
4. **Non-Negative Amounts**: Booking amount, ACV, and TCV must be non-negative values
5. **Positive Quantities**: Quantity must be a positive integer
6. **Discount Range**: Discount percentage must be between 0 and 1 (fractional representation)
7. **Renewal Classification**: is_renewal flag indicates whether the booking is a renewal (1) or net new (0)
8. **ACV Calculation**: ACV represents the annualized value of the contract
9. **TCV Calculation**: TCV represents the total value over the full contract term
10. **Booking Amount Calculation**: Booking amount equals quantity × unit list price × (1 - discount percentage)

---

## Attribute Definitions

### booking_id
Unique identifier for an individual booking transaction record. Serves as the primary key for the bookings fact table.

### order_number
Sales order number associated with the booking transaction. Multiple booking records may share the same order number if the order contains multiple line items.

### order_line_number
Line number within the sales order representing the booked item or service. Combined with order_number, this provides a unique business identifier.

### date_key
Foreign key linking the booking transaction to the reporting date dimension. Used for time-based analysis and fiscal period reporting.

### customer_key
Foreign key linking the booking transaction to the customer dimension. Enables analysis by customer segment, industry, and account tier.

### product_key
Foreign key linking the booking transaction to the product dimension. Enables analysis by product family, technology domain, and offer type.

### partner_key
Foreign key linking the booking transaction to the partner dimension. Enables analysis by partner type, tier, and route to market.

### geography_key
Foreign key linking the booking transaction to the geography dimension. Enables analysis by region, theater, and country.

### sales_rep_key
Foreign key linking the booking transaction to the sales representative dimension. Enables analysis by sales role, team, and segment coverage.

### contract_key
Foreign key linking the booking transaction to the contract dimension. Enables analysis by contract type, term, and coverage level.

### booking_type
Type of booking event, such as new business or renewal. Provides categorical classification of the booking transaction.

### is_renewal
Indicator showing whether the booking transaction is a renewal (1) or net new business (0). Used to separate renewal revenue from new customer acquisition.

### quantity
Number of units, licenses, or services booked in the transaction. Used to calculate volume metrics and average selling prices.

### unit_list_price_usd
Standard list price per unit in US dollars before discounts. Represents the published price for the product or service.

### discount_pct
Discount applied to the booked item or service, stored as a fractional percentage of list price (e.g., 0.15 represents 15% discount).

### booking_amount_usd
Total booked sales amount in US dollars after pricing and discount adjustments. Primary revenue metric for the booking transaction.

### acv_usd
Annualized contract value of the booking in US dollars. Represents the annual recurring revenue value for subscription and recurring revenue analysis.

### tcv_usd
Total contract value of the booking over the full contract term in US dollars. Represents the total revenue expected over the life of the contract.

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Usage Examples

### Revenue Analysis
- Calculate total booking amount by fiscal quarter
- Compare ACV vs TCV trends over time
- Analyze renewal vs net new revenue composition

### Volume Analysis
- Track booking count by product family
- Monitor quantity trends by customer segment
- Analyze order count by sales representative

### Pricing Analysis
- Calculate average discount percentage by partner type
- Track average selling price trends by geography
- Monitor unit list price changes over time

### Performance Analysis
- Identify top customers by booking amount
- Rank products by total quantity sold
- Evaluate sales representative productivity

---

## Data Quality Checks

- booking_id is unique and not null
- All foreign keys reference valid dimension records
- booking_amount_usd is non-negative
- acv_usd is non-negative
- tcv_usd is non-negative
- quantity is positive
- discount_pct is between 0 and 1
- is_renewal is either 0 or 1
- date_key references a valid date
