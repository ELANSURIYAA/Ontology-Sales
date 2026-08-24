---
title: Sales Bookings and Revenue Analytics
type: domain
description: Sales bookings and revenue analytics semantic model for completed booking transactions
resource: domains
tags: [sales, bookings, revenue, analytics, domain]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Bookings and Revenue Analytics

## Business Definition

Sales bookings and revenue analytics semantic model for completed booking transactions across customers, products, partners, geographies, sales representatives, contracts, and reporting periods.

---

## Business Purpose

This domain enables comprehensive analysis of sales booking performance, revenue recognition, contract values, and business relationships across multiple dimensions including customer segments, product portfolios, partner channels, geographic territories, and time periods.

The domain supports strategic decision-making for:
- Sales performance tracking and forecasting
- Revenue pipeline analysis
- Customer and product profitability analysis
- Partner channel effectiveness
- Geographic market penetration
- Sales representative productivity
- Contract and renewal management

---

## AI Context

Use this semantic model for sales booking and revenue analysis. Booking transactions are represented at the booking transaction grain in the bookings dataset. Use booking date for time-based analysis and the defined metrics for booking amount, ACV, TCV, quantity, discount, renewal, and order analysis.

---

## Related Entities

### Fact Entity
- [Bookings](../entities/bookings.md) - Individual completed sales booking transactions

### Dimension Entities
- [Customers](../entities/customers.md) - Customer organizations placing orders
- [Products](../entities/products.md) - Products and offers sold
- [Partners](../entities/partners.md) - Sales partners and channels
- [Geographies](../entities/geographies.md) - Geographic sales territories
- [Sales Representatives](../entities/sales-representatives.md) - Sales personnel
- [Contracts](../entities/contracts.md) - Commercial agreements
- [Dates](../entities/dates.md) - Calendar and fiscal time periods

---

## Related Measures

### Volume Metrics
- [Booking Count](../measures/booking-count.md)
- [Distinct Order Count](../measures/distinct-order-count.md)
- [Total Quantity](../measures/total-quantity.md)

### Revenue Metrics
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)

### Pricing Metrics
- [Average Discount Pct](../measures/average-discount-pct.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

### Business Type Metrics
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

---

## Related Relationships

- [Bookings to Customers](../relationships/bookings-to-customers.md)
- [Bookings to Products](../relationships/bookings-to-products.md)
- [Bookings to Partners](../relationships/bookings-to-partners.md)
- [Bookings to Geographies](../relationships/bookings-to-geographies.md)
- [Bookings to Sales Representatives](../relationships/bookings-to-sales-representatives.md)
- [Bookings to Contracts](../relationships/bookings-to-contracts.md)
- [Bookings to Dates](../relationships/bookings-to-dates.md)

---

## Key Business Concepts

- [Booking Transaction](../glossary/booking-transaction.md)
- [Annual Contract Value](../glossary/annual-contract-value.md)
- [Total Contract Value](../glossary/total-contract-value.md)
- [Renewal](../glossary/renewal.md)
- [Net New Business](../glossary/net-new-business.md)
- [Customer Segment](../glossary/customer-segment.md)
- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Route to Market](../glossary/route-to-market.md)
- [Fiscal Period](../glossary/fiscal-period.md)

---

## Technical Architecture

**Source System**: quotetobooking

**Data Model Pattern**: Star Schema

**Grain**: Individual booking transaction

---

## Navigation

- [Return to Domains Index](index.md)
- [Return to Main Index](../index.md)
- [View Semantic Summary](../semantic_summary.md)
