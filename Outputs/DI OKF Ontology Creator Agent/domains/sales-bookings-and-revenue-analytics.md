---
title: Sales Bookings and Revenue Analytics
type: domain
description: Sales bookings and revenue analytics semantic model for completed booking transactions across customers, products, partners, geographies, sales representatives, contracts, and reporting periods
resource: domains
tags: [sales, bookings, revenue, analytics, domain]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Bookings and Revenue Analytics

## Business Definition

The Sales Bookings and Revenue Analytics domain encompasses all business activities related to capturing, tracking, and analyzing completed sales booking transactions. This domain provides a comprehensive view of sales performance across multiple business dimensions including customers, products, partners, geographic territories, sales representatives, contracts, and time periods.

---

## Business Purpose

This domain enables organizations to:

- **Track Sales Performance**: Monitor booking volumes, revenue amounts, and transaction counts across all dimensions
- **Analyze Revenue Trends**: Understand revenue patterns over time using calendar and fiscal periods
- **Measure Customer Value**: Analyze booking behavior by customer segment, industry, and account tier
- **Evaluate Product Performance**: Assess product family and technology domain performance
- **Optimize Channel Strategy**: Evaluate partner effectiveness and route-to-market performance
- **Monitor Geographic Distribution**: Track sales performance across regions, theaters, and countries
- **Assess Sales Productivity**: Measure sales representative performance by role, team, and segment
- **Manage Contracts**: Analyze contract types, terms, and renewal behavior
- **Track Pricing Effectiveness**: Monitor discount trends and average selling prices
- **Distinguish Revenue Types**: Separate renewal revenue from net new business

---

## Domain Scope

### Grain
The domain operates at the **booking transaction grain**, where each record represents a single completed booking transaction with associated financial measures and dimensional attributes.

### Source Systems
- **Primary Source**: quotetobooking schema
- **Fact Table**: quotetobooking.fact_bookings
- **Dimension Tables**: dim_customer, dim_product, dim_partner, dim_geography, dim_sales_rep, dim_contract, dim_date

---

## Related Entities

### Fact Entity
- **[Bookings](../entities/bookings.md)**: Core fact table capturing individual completed sales booking transactions and their associated financial measures, quantities, renewal status, and links to related business dimensions

### Dimension Entities
- **[Customers](../entities/customers.md)**: Customer information including segment, industry, account tier, and headquarters location
- **[Products](../entities/products.md)**: Product information including family, technology domain, offer type, and business entity
- **[Partners](../entities/partners.md)**: Partner information including type, tier, and route to market
- **[Geographies](../entities/geographies.md)**: Geographic sales territory attributes including region, theater, and country
- **[Sales Representatives](../entities/sales-representatives.md)**: Sales representative information including role, team, and segment coverage
- **[Contracts](../entities/contracts.md)**: Contract information including type, term duration, renewal behavior, and coverage level
- **[Dates](../entities/dates.md)**: Calendar and fiscal time attributes for temporal analysis

---

## Related Measures

### Volume Measures
- **[Booking Count](../measures/booking-count.md)**: Count of booking transaction records
- **[Distinct Order Count](../measures/distinct-order-count.md)**: Count of distinct sales orders
- **[Total Quantity](../measures/total-quantity.md)**: Total units, licenses, or services booked

### Revenue Measures
- **[Total Booking Amount USD](../measures/total-booking-amount-usd.md)**: Total booked sales amount after pricing and discount adjustments
- **[Total ACV USD](../measures/total-acv-usd.md)**: Total annual contract value
- **[Total TCV USD](../measures/total-tcv-usd.md)**: Total contract value over full term

### Pricing Measures
- **[Average Discount Percentage](../measures/average-discount-pct.md)**: Average discount applied to bookings
- **[Average Selling Price USD](../measures/average-selling-price-usd.md)**: Average revenue per unit sold
- **[Average Booking Value USD](../measures/average-booking-value-usd.md)**: Average booking value per transaction

### Renewal Measures
- **[Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)**: Total renewal booking amount
- **[Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)**: Total net new booking amount

---

## Related Relationships

- **[Bookings to Contracts](../relationships/bookings-to-contracts.md)**: Links booking transactions to contract terms and conditions
- **[Bookings to Customers](../relationships/bookings-to-customers.md)**: Links booking transactions to customer accounts
- **[Bookings to Dates](../relationships/bookings-to-dates.md)**: Links booking transactions to time periods
- **[Bookings to Geographies](../relationships/bookings-to-geographies.md)**: Links booking transactions to geographic territories
- **[Bookings to Partners](../relationships/bookings-to-partners.md)**: Links booking transactions to sales partners
- **[Bookings to Products](../relationships/bookings-to-products.md)**: Links booking transactions to products
- **[Bookings to Sales Representatives](../relationships/bookings-to-sales-representatives.md)**: Links booking transactions to sales representatives

---

## Key Business Concepts

### [Booking Transaction](../glossary/booking-transaction.md)
A completed sales transaction representing the commitment to purchase products or services

### [Annual Contract Value](../glossary/annual-contract-value.md)
The annualized revenue value of a contract for subscription and recurring revenue analysis

### [Total Contract Value](../glossary/total-contract-value.md)
The full contract value over the entire contract term for long-term revenue planning

### [Renewal](../glossary/renewal.md)
A booking transaction representing the continuation of an existing customer contract

### [Net New Business](../glossary/net-new-business.md)
A booking transaction representing new customer acquisition or expansion

### [Customer Segment](../glossary/customer-segment.md)
Market segment classification such as Enterprise, Service Provider, or Public Sector

### [Product Family](../glossary/product-family.md)
Higher-level grouping of related products within the portfolio

### [Technology Domain](../glossary/technology-domain.md)
Technology area or solution domain the product belongs to

### [Partner Type](../glossary/partner-type.md)
Classification of partner such as distributor, reseller, or systems integrator

### [Route to Market](../glossary/route-to-market.md)
Sales channel path through which products or services are sold to customers

---

## Business Rules

1. **Booking Transaction Grain**: Each booking record represents a single completed transaction at the order line level
2. **Revenue Recognition**: Booking amount represents committed revenue at the time of booking completion
3. **ACV Calculation**: Annual Contract Value is calculated by annualizing the total contract value over the contract term
4. **Renewal Classification**: Bookings are classified as renewal when is_renewal flag equals 1
5. **Discount Application**: Discounts are stored as fractional percentages and applied to list prices
6. **Foreign Key Integrity**: All foreign keys must reference valid dimension records
7. **Time Attribution**: Booking transactions are attributed to time periods using the date_key

---

## Analytical Use Cases

### Sales Performance Analysis
- Track booking trends over time by fiscal period
- Compare actual bookings against targets and quotas
- Identify top-performing products, customers, and sales representatives

### Revenue Forecasting
- Project future revenue based on ACV and TCV trends
- Analyze renewal rates and customer retention
- Model revenue scenarios by segment and product

### Customer Analytics
- Segment customers by booking behavior and value
- Identify high-value customer accounts
- Analyze customer lifetime value and retention

### Product Analytics
- Evaluate product family performance and profitability
- Identify cross-sell and upsell opportunities
- Track technology domain adoption trends

### Channel Analytics
- Assess partner contribution to revenue
- Optimize route-to-market strategies
- Evaluate channel effectiveness by geography

### Pricing Analytics
- Monitor discount trends and pricing effectiveness
- Analyze price elasticity by segment and product
- Optimize pricing strategies to maximize revenue

---

## Data Quality Requirements

- All booking transactions must have valid foreign keys to dimension tables
- Booking amounts must be non-negative
- Quantities must be positive integers
- Discount percentages must be between 0 and 1
- ACV and TCV must be consistent with booking amount and contract term
- Date keys must reference valid dates in the date dimension
- Primary keys must be unique and non-null

---

## Semantic Links

- [Domain Index](./index.md)
- [Entities Index](../entities/index.md)
- [Relationships Index](../relationships/index.md)
- [Measures Index](../measures/index.md)
- [Glossary Index](../glossary/index.md)
- [Semantic Summary](../semantic_summary.md)
- [Knowledge Bundle Index](../index.md)
