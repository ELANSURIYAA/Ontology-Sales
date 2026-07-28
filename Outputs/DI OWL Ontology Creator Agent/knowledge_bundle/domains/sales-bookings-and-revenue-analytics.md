---
title: Sales Bookings and Revenue Analytics
type: domain
description: Sales booking operations for enterprise networking, security, collaboration, observability, and software subscription products
resource: domains
tags: [domain, sales, bookings, revenue, analytics, enterprise]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Bookings and Revenue Analytics

## Business Definition

This domain represents sales booking operations for enterprise networking, security, collaboration, observability, and software subscription products. It captures completed customer bookings and supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods.

---

## Business Purpose

The Sales Bookings and Revenue Analytics domain enables the organization to:

- Track and analyze completed sales bookings across all product lines
- Measure sales performance by customer segment, geography, and product family
- Evaluate partner and sales representative effectiveness
- Monitor contract terms, renewal behavior, and support coverage
- Analyze pricing, discounting, and revenue trends
- Support fiscal and calendar-based reporting
- Calculate key revenue metrics including booking amount, ACV, and TCV

---

## Related Entities

This domain contains the following business entities:

### Dimension Entities

- **[Contract](../entities/contract.md)**: Commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level
- **[Customer](../entities/customer.md)**: Customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location
- **[Date](../entities/date.md)**: Calendar and fiscal date attributes used to analyze bookings over time
- **[Geography](../entities/geography.md)**: Geographic attributes used to analyze bookings by sales region, theater, and country
- **[Partner](../entities/partner.md)**: Channel and direct partners involved in the sales process, including partner type, tier, and route to market
- **[Product](../entities/product.md)**: Products and offers sold to customers, including product family, technology domain, offer type, and business entity
- **[Sales Representative](../entities/sales-representative.md)**: Sales personnel responsible for managing customer relationships and booking transactions

### Fact Entities

- **[Booking Transaction](../entities/booking-transaction.md)**: Individual completed sales booking transactions with related financial measures and links to all dimension entities

---

## Related Measures

This domain supports the following business measures:

- **[Quantity Sold](../measures/quantity-sold.md)**: Number of units, licenses, or subscriptions included in booking transactions
- **[Unit List Price USD](../measures/unit-list-price-usd.md)**: Standard list price per unit before discounts are applied
- **[Discount Percentage](../measures/discount-percentage.md)**: Percentage discount applied to the list price
- **[Booking Amount USD](../measures/booking-amount-usd.md)**: Total booked revenue amount after pricing adjustments
- **[Annual Contract Value USD](../measures/annual-contract-value-usd.md)**: Annualized value of the contract
- **[Total Contract Value USD](../measures/total-contract-value-usd.md)**: Total value of the full contract

---

## Related Relationships

The domain is structured around the following key relationships:

- [Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)
- [Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)
- [Date to Booking Transaction](../relationships/date-to-booking-transaction.md)
- [Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)
- [Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)
- [Product to Booking Transaction](../relationships/product-to-booking-transaction.md)
- [Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)

---

## Semantic Links

### Related Glossary Concepts

- [Booking Transaction](../glossary/booking-transaction.md)
- [Booking Amount USD](../glossary/booking-amount-usd.md)
- [Annual Contract Value USD](../glossary/annual-contract-value-usd.md)
- [Total Contract Value USD](../glossary/total-contract-value-usd.md)
- [Customer Segment](../glossary/customer-segment.md)
- [Product Family](../glossary/product-family.md)
- [Partner Type](../glossary/partner-type.md)
- [Sales Region](../glossary/sales-region.md)
- [Contract Type](../glossary/contract-type.md)
- [Fiscal Year](../glossary/fiscal-year.md)

---

## Technical Mapping

**Source System**: QuoteToBooking

**Database Tables**:
- QuoteToBooking.dim_contract
- QuoteToBooking.dim_customer
- QuoteToBooking.dim_date
- QuoteToBooking.dim_geography
- QuoteToBooking.dim_partner
- QuoteToBooking.dim_product
- QuoteToBooking.dim_sales_rep
- QuoteToBooking.fact_bookings

---

## Business Rules

1. Every booking transaction must be associated with a valid customer
2. Every booking transaction must be associated with a valid product
3. Every booking transaction must have a booking date
4. Booking amounts are recorded in U.S. dollars
5. Annual Contract Value (ACV) represents annualized contract value
6. Total Contract Value (TCV) represents full contract commitment
7. Discount percentages are applied to list prices to calculate booking amounts
8. Renewal indicator identifies repeat business from existing customers
9. Contract terms are measured in months
10. All financial measures use numeric data types for precision

---

## Domain Statistics

- **Entities**: 8 (7 dimensions, 1 fact)
- **Attributes**: 61
- **Relationships**: 7
- **Measures**: 6
- **Glossary Terms**: 69
- **Primary Keys**: 8
- **Foreign Keys**: 7

---

## Navigation

- [Back to Domains Index](index.md)
- [Back to Main Index](../index.md)
- [View Entities](../entities/index.md)
- [View Measures](../measures/index.md)
- [View Relationships](../relationships/index.md)
