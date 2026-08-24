---
title: Semantic Summary
type: index
description: High-level overview of the sales bookings and revenue analytics semantic model
resource: knowledge_bundle
tags: [semantic, summary, overview, model]
timestamp: 2026-07-28T00:00:00Z
---

# Semantic Summary

## Model Overview

**Name**: Sales Bookings and Revenue Analytics

**Description**: Sales bookings and revenue analytics semantic model for completed booking transactions across customers, products, partners, geographies, sales representatives, contracts, and reporting periods.

---

## AI Context

Use this semantic model for sales booking and revenue analysis. Booking transactions are represented at the booking transaction grain in the bookings dataset. Use booking date for time-based analysis and the defined metrics for booking amount, ACV, TCV, quantity, discount, renewal, and order analysis.

---

## Business Domains

- [Sales Bookings and Revenue Analytics](domains/sales-bookings-and-revenue-analytics.md)

---

## Core Entities

### Fact Entity
- [Bookings](entities/bookings.md) - Captures individual completed sales booking transactions and their associated financial measures

### Dimension Entities
- [Customers](entities/customers.md) - Customer organizations that place orders
- [Products](entities/products.md) - Products and offers sold to customers
- [Partners](entities/partners.md) - Direct and indirect sales partners
- [Geographies](entities/geographies.md) - Geographic sales territories
- [Sales Representatives](entities/sales-representatives.md) - Sales personnel managing customer relationships
- [Contracts](entities/contracts.md) - Commercial agreements and service coverage terms
- [Dates](entities/dates.md) - Calendar and fiscal time attributes

---

## Key Relationships

The semantic model follows a star schema pattern with **Bookings** as the central fact entity:

- Bookings → Customers (many-to-one)
- Bookings → Products (many-to-one)
- Bookings → Partners (many-to-one)
- Bookings → Geographies (many-to-one)
- Bookings → Sales Representatives (many-to-one)
- Bookings → Contracts (many-to-one)
- Bookings → Dates (many-to-one)

---

## Core Measures

### Volume Metrics
- [Booking Count](measures/booking-count.md)
- [Distinct Order Count](measures/distinct-order-count.md)
- [Total Quantity](measures/total-quantity.md)

### Revenue Metrics
- [Total Booking Amount USD](measures/total-booking-amount-usd.md)
- [Total ACV USD](measures/total-acv-usd.md)
- [Total TCV USD](measures/total-tcv-usd.md)

### Pricing Metrics
- [Average Discount Pct](measures/average-discount-pct.md)
- [Average Selling Price USD](measures/average-selling-price-usd.md)
- [Average Booking Value USD](measures/average-booking-value-usd.md)

### Business Type Metrics
- [Renewal Booking Amount USD](measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](measures/net-new-booking-amount-usd.md)

---

## Key Business Concepts

- [Booking Transaction](glossary/booking-transaction.md)
- [Annual Contract Value](glossary/annual-contract-value.md)
- [Total Contract Value](glossary/total-contract-value.md)
- [Renewal](glossary/renewal.md)
- [Net New Business](glossary/net-new-business.md)
- [Customer Segment](glossary/customer-segment.md)
- [Product Family](glossary/product-family.md)
- [Technology Domain](glossary/technology-domain.md)
- [Route to Market](glossary/route-to-market.md)
- [Fiscal Period](glossary/fiscal-period.md)

---

## Technical Architecture

**Source System**: quotetobooking

**Grain**: Individual booking transaction

**Primary Fact Table**: quotetobooking.fact_bookings

**Dimension Tables**:
- quotetobooking.dim_customer
- quotetobooking.dim_product
- quotetobooking.dim_partner
- quotetobooking.dim_geography
- quotetobooking.dim_sales_rep
- quotetobooking.dim_contract
- quotetobooking.dim_date

---

## Navigation

- [Return to Index](index.md)
- [View All Metrics](metrics.md)
- [Browse Domains](domains/index.md)
- [Browse Entities](entities/index.md)
- [Browse Relationships](relationships/index.md)
- [Browse Measures](measures/index.md)
- [Browse Glossary](glossary/index.md)
