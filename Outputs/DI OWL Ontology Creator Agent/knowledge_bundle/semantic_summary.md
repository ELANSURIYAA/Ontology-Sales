---
title: Semantic Summary - Sales Bookings and Revenue Analytics
type: summary
description: Complete semantic model overview for Sales Bookings and Revenue Analytics
resource: knowledge_bundle
tags: [semantic, summary, sales, bookings, revenue, analytics]
timestamp: 2026-07-28T00:00:00Z
---

# Semantic Summary - Sales Bookings and Revenue Analytics

This document provides a comprehensive overview of the semantic model for Sales Bookings and Revenue Analytics.

---

## Domain Overview

### Sales Bookings and Revenue Analytics

This domain represents sales booking operations for enterprise networking, security, collaboration, observability, and software subscription products. It captures completed customer bookings and supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods.

**Related Entities**: Contract, Customer, Date, Geography, Partner, Product, Sales Representative, Booking Transaction

**Related Measures**: Quantity Sold, Unit List Price USD, Discount Percentage, Booking Amount USD, Annual Contract Value USD, Total Contract Value USD

---

## Entity Summary

| Entity | Type | Description | Key Relationships |
|--------|------|-------------|-------------------|
| [Contract](entities/contract.md) | Dimension | Commercial agreements associated with bookings | Booking Transaction |
| [Customer](entities/customer.md) | Dimension | Customers that place orders and generate bookings | Booking Transaction |
| [Date](entities/date.md) | Dimension | Calendar and fiscal date attributes | Booking Transaction |
| [Geography](entities/geography.md) | Dimension | Geographic attributes for sales analysis | Booking Transaction |
| [Partner](entities/partner.md) | Dimension | Channel and direct partners in sales process | Booking Transaction |
| [Product](entities/product.md) | Dimension | Products and offers sold to customers | Booking Transaction |
| [Sales Representative](entities/sales-representative.md) | Dimension | Sales personnel managing customer relationships | Booking Transaction |
| [Booking Transaction](entities/booking-transaction.md) | Fact | Individual completed sales booking transactions | Contract, Customer, Date, Geography, Partner, Product, Sales Representative |

---

## Relationship Summary

| Relationship | Source | Target | Cardinality | Type |
|--------------|--------|--------|-------------|------|
| [Contract to Booking Transaction](relationships/contract-to-booking-transaction.md) | Contract | Booking Transaction | One-to-Many | Foreign Key |
| [Customer to Booking Transaction](relationships/customer-to-booking-transaction.md) | Customer | Booking Transaction | One-to-Many | Foreign Key |
| [Date to Booking Transaction](relationships/date-to-booking-transaction.md) | Date | Booking Transaction | One-to-Many | Foreign Key |
| [Geography to Booking Transaction](relationships/geography-to-booking-transaction.md) | Geography | Booking Transaction | One-to-Many | Foreign Key |
| [Partner to Booking Transaction](relationships/partner-to-booking-transaction.md) | Partner | Booking Transaction | One-to-Many | Foreign Key |
| [Product to Booking Transaction](relationships/product-to-booking-transaction.md) | Product | Booking Transaction | One-to-Many | Foreign Key |
| [Sales Representative to Booking Transaction](relationships/sales-representative-to-booking-transaction.md) | Sales Representative | Booking Transaction | One-to-Many | Foreign Key |

---

## Measure Summary

| Measure | Entity | Aggregation | Description |
|---------|--------|-------------|-------------|
| [Quantity Sold](measures/quantity-sold.md) | Booking Transaction | SUM | Number of units, licenses, or subscriptions |
| [Unit List Price USD](measures/unit-list-price-usd.md) | Booking Transaction | SUM | Standard list price per unit before discounts |
| [Discount Percentage](measures/discount-percentage.md) | Booking Transaction | AVG | Percentage discount applied to list price |
| [Booking Amount USD](measures/booking-amount-usd.md) | Booking Transaction | SUM | Total booked revenue after pricing adjustments |
| [Annual Contract Value USD](measures/annual-contract-value-usd.md) | Booking Transaction | SUM | Annualized value of the contract |
| [Total Contract Value USD](measures/total-contract-value-usd.md) | Booking Transaction | SUM | Total value of the full contract |

---

## Glossary Summary

The glossary contains 69 business terms covering:

- **Contract Terms**: Contract, Contract Key, Contract Type, Contract Term Months, Auto Renew Flag, Coverage Level
- **Customer Terms**: Customer, Customer Key, Customer ID, Customer Name, Customer Segment, Industry, Account Tier, Headquarters Country, Headquarters Region
- **Date Terms**: Date, Date Key, Full Date, Month Name, Calendar Year, Fiscal Year, Fiscal Quarter, Fiscal Period Sequence
- **Geography Terms**: Geography, Geography Key, Sales Region, Sales Theater, Country
- **Partner Terms**: Partner, Partner Key, Partner ID, Partner Name, Partner Type, Partner Tier, Route to Market
- **Product Terms**: Product, Product Key, Product ID, Product Name, Product Family, Technology Domain, Offer Type, Business Entity
- **Sales Representative Terms**: Sales Representative, Sales Representative Key, Sales Representative ID, Sales Representative Name, Sales Role, Sales Team, Covered Segment
- **Booking Transaction Terms**: Booking Transaction, Booking ID, Order Number, Order Line Number, Booking Date Key, Booking Type, Renewal Indicator, Quantity Sold, Unit List Price USD, Discount Percentage, Booking Amount USD, Annual Contract Value USD, Total Contract Value USD

See [Glossary Index](glossary/index.md) for complete definitions.

---

## Semantic Model Statistics

- **Domains**: 1
- **Entities**: 8
- **Attributes**: 61
- **Relationships**: 7
- **Measures**: 6
- **Glossary Terms**: 69
- **Primary Keys**: 8
- **Foreign Keys**: 7

---

## Technical Mapping

**Source System**: QuoteToBooking

**Tables**:
- dim_contract
- dim_customer
- dim_date
- dim_geography
- dim_partner
- dim_product
- dim_sales_rep
- fact_bookings

---

## Semantic Integrity

- All entities have primary keys
- All relationships are properly defined
- All measures have aggregation types
- All glossary terms are mapped to technical columns
- All foreign keys reference valid dimension tables
- Confidence scores range from 0.95 to 1.00

---

## Navigation

- [Back to Index](index.md)
- [View Metrics](metrics.md)
- [Browse Domains](domains/index.md)
- [Browse Entities](entities/index.md)
- [Browse Relationships](relationships/index.md)
- [Browse Measures](measures/index.md)
- [Browse Glossary](glossary/index.md)
