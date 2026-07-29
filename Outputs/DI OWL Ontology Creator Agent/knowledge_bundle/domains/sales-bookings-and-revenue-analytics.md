---
title: Sales Bookings and Revenue Analytics
type: domain
description: Sales booking operations for enterprise products supporting analysis across customers, products, partners, geographies, and contracts
resource: domains
tags: [sales, bookings, revenue, analytics, enterprise, domain]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Bookings and Revenue Analytics

## Business Definition

The Sales Bookings and Revenue Analytics domain represents sales booking operations for enterprise networking, security, collaboration, observability, and software subscription products. This domain captures completed customer bookings and supports comprehensive analysis of sales performance across multiple business dimensions.

---

## Business Purpose

This domain serves as the foundation for:

- **Sales Performance Analysis** - Track and analyze booking performance across time, geography, and sales teams
- **Revenue Analytics** - Monitor booking amounts, contract values, and revenue metrics
- **Customer Intelligence** - Analyze customer segments, industries, and account tiers
- **Product Portfolio Management** - Evaluate product family performance and technology domain adoption
- **Partner Channel Analysis** - Assess partner contribution and route-to-market effectiveness
- **Contract Management** - Track contract types, terms, and renewal behavior
- **Strategic Planning** - Support forecasting, quota setting, and resource allocation

---

## Domain Scope

### Included

- Completed sales bookings
- Customer account information
- Product and offer catalog
- Partner and channel data
- Geographic sales territories
- Sales representative assignments
- Contract terms and conditions
- Financial measures (bookings, ACV, TCV)
- Calendar and fiscal time periods

### Excluded

- Quote and opportunity pipeline
- Order fulfillment and delivery
- Revenue recognition accounting
- Customer support and service
- Product usage and consumption
- Billing and invoicing
- Collections and accounts receivable

---

## Related Entities

### Dimension Entities

- **[Contract](../entities/contract.md)** - Commercial agreements and contract terms
- **[Customer](../entities/customer.md)** - Customer organizations and account information
- **[Date](../entities/date.md)** - Calendar and fiscal time periods
- **[Geography](../entities/geography.md)** - Sales regions, theaters, and countries
- **[Partner](../entities/partner.md)** - Channel and direct partner organizations
- **[Product](../entities/product.md)** - Products and subscription offers
- **[Sales Representative](../entities/sales-representative.md)** - Sales personnel and team assignments

### Fact Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Individual sales booking records with financial measures

---

## Related Measures

### Volume Metrics

- **[Quantity Sold](../measures/quantity-sold.md)** - Units, licenses, or subscriptions sold

### Pricing Metrics

- **[Unit List Price USD](../measures/unit-list-price-usd.md)** - Standard list price per unit
- **[Discount Percentage](../measures/discount-percentage.md)** - Price discount percentage

### Revenue Metrics

- **[Booking Amount USD](../measures/booking-amount-usd.md)** - Total booked revenue
- **[Annual Contract Value USD](../measures/annual-contract-value-usd.md)** - Annualized contract value
- **[Total Contract Value USD](../measures/total-contract-value-usd.md)** - Total contract value

---

## Related Relationships

The domain implements a dimensional star schema with the following relationships:

- **[Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)** - Links contracts to booking records
- **[Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)** - Links customers to booking records
- **[Date to Booking Transaction](../relationships/date-to-booking-transaction.md)** - Links dates to booking records
- **[Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)** - Links geographies to booking records
- **[Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)** - Links partners to booking records
- **[Product to Booking Transaction](../relationships/product-to-booking-transaction.md)** - Links products to booking records
- **[Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)** - Links sales reps to booking records

---

## Business Rules

### Data Quality Rules

1. Every booking transaction must have a valid customer
2. Every booking transaction must have a valid product
3. Every booking transaction must have a valid date
4. Booking amounts must be non-negative
5. Contract terms must be positive integers
6. Discount percentages must be between 0 and 100

### Business Logic Rules

1. Annual Contract Value (ACV) = Total Contract Value (TCV) ÷ Contract Term (Years)
2. Booking Amount = Quantity × Unit List Price × (1 - Discount Percentage)
3. Renewal bookings must reference an existing contract
4. New bookings create new contract records
5. Fiscal periods follow company fiscal calendar

### Referential Integrity Rules

1. All foreign keys must reference valid dimension records
2. Dimension surrogate keys must be unique
3. Business keys must be unique within entity
4. Date keys must exist in date dimension
5. Geographic hierarchies must be consistent

---

## Analytical Capabilities

### Dimensional Analysis

- **Time Analysis** - Trend analysis by calendar and fiscal periods
- **Geographic Analysis** - Performance by region, theater, and country
- **Customer Analysis** - Segmentation by industry, segment, and tier
- **Product Analysis** - Portfolio analysis by family and technology domain
- **Partner Analysis** - Channel performance by type, tier, and route
- **Contract Analysis** - Contract mix by type, term, and coverage
- **Sales Analysis** - Representative and team performance tracking

### Measure Analysis

- **Revenue Analysis** - Booking amounts, ACV, and TCV tracking
- **Volume Analysis** - Quantity and unit analysis
- **Pricing Analysis** - List price and discount effectiveness
- **Growth Analysis** - Period-over-period comparisons
- **Mix Analysis** - Product, customer, and channel mix
- **Performance Analysis** - Quota attainment and target achievement

---

## Technical Mapping

### Source System

**Database**: QuoteToBooking  
**Schema**: Dimensional star schema  
**Tables**: 8 (7 dimensions + 1 fact)

### Table Mapping

| Entity | Technical Table |
|--------|----------------|
| Contract | QuoteToBooking.dim_contract |
| Customer | QuoteToBooking.dim_customer |
| Date | QuoteToBooking.dim_date |
| Geography | QuoteToBooking.dim_geography |
| Partner | QuoteToBooking.dim_partner |
| Product | QuoteToBooking.dim_product |
| Sales Representative | QuoteToBooking.dim_sales_rep |
| Booking Transaction | QuoteToBooking.fact_bookings |

---

## Domain Statistics

| Metric | Count |
|--------|-------|
| Entities | 8 |
| Attributes | 61 |
| Relationships | 7 |
| Measures | 6 |
| Primary Keys | 8 |
| Foreign Keys | 7 |

---

## Semantic Links

- [Domain Index](./index.md)
- [Entity Index](../entities/index.md)
- [Relationship Index](../relationships/index.md)
- [Measure Index](../measures/index.md)
- [Glossary Index](../glossary/index.md)
- [Semantic Summary](../semantic_summary.md)
- [Main Index](../index.md)

---

## Metadata

**Domain ID**: DOM001  
**Domain Type**: Analytical  
**Model Pattern**: Star Schema  
**Source System**: QuoteToBooking  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
