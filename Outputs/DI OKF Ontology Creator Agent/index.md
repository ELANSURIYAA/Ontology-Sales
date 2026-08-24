---
title: Sales Bookings and Revenue Analytics Knowledge Bundle
type: index
description: Complete OKF knowledge bundle for sales bookings and revenue analytics semantic model
resource: knowledge_bundle
tags: [sales, bookings, revenue, analytics, okf, knowledge-bundle]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Bookings and Revenue Analytics Knowledge Bundle

## Overview

This knowledge bundle contains the complete semantic model for sales bookings and revenue analytics. It captures completed booking transactions across customers, products, partners, geographies, sales representatives, contracts, and reporting periods.

---

## Business Context

The sales bookings and revenue analytics semantic model provides a comprehensive view of sales performance, enabling analysis of booking transactions at the booking transaction grain. The model supports time-based analysis using booking dates and includes defined metrics for booking amount, ACV, TCV, quantity, discount, renewal, and order analysis.

---

## Knowledge Bundle Structure

### [Semantic Summary](./semantic_summary.md)
Complete overview of the semantic model architecture, domains, entities, and relationships.

### [Metrics Summary](./metrics.md)
Comprehensive catalog of all business measures and KPIs.

### [Domains](./domains/index.md)
Business domain documentation:
- [Sales Bookings and Revenue Analytics](./domains/sales-bookings-and-revenue-analytics.md)

### [Entities](./entities/index.md)
Business entity documentation:
- [Bookings](./entities/bookings.md)
- [Customers](./entities/customers.md)
- [Products](./entities/products.md)
- [Partners](./entities/partners.md)
- [Geographies](./entities/geographies.md)
- [Sales Representatives](./entities/sales-representatives.md)
- [Contracts](./entities/contracts.md)
- [Dates](./entities/dates.md)

### [Relationships](./relationships/index.md)
Business relationship documentation:
- [Bookings to Contracts](./relationships/bookings-to-contracts.md)
- [Bookings to Customers](./relationships/bookings-to-customers.md)
- [Bookings to Dates](./relationships/bookings-to-dates.md)
- [Bookings to Geographies](./relationships/bookings-to-geographies.md)
- [Bookings to Partners](./relationships/bookings-to-partners.md)
- [Bookings to Products](./relationships/bookings-to-products.md)
- [Bookings to Sales Representatives](./relationships/bookings-to-sales-representatives.md)

### [Measures](./measures/index.md)
Business measure documentation:
- [Booking Count](./measures/booking-count.md)
- [Distinct Order Count](./measures/distinct-order-count.md)
- [Total Quantity](./measures/total-quantity.md)
- [Total Booking Amount USD](./measures/total-booking-amount-usd.md)
- [Total ACV USD](./measures/total-acv-usd.md)
- [Total TCV USD](./measures/total-tcv-usd.md)
- [Average Discount Percentage](./measures/average-discount-pct.md)
- [Average Selling Price USD](./measures/average-selling-price-usd.md)
- [Renewal Booking Amount USD](./measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](./measures/net-new-booking-amount-usd.md)
- [Average Booking Value USD](./measures/average-booking-value-usd.md)

### [Glossary](./glossary/index.md)
Business terminology and definitions:
- [Booking Transaction](./glossary/booking-transaction.md)
- [Annual Contract Value](./glossary/annual-contract-value.md)
- [Total Contract Value](./glossary/total-contract-value.md)
- [Renewal](./glossary/renewal.md)
- [Net New Business](./glossary/net-new-business.md)
- [Booking Amount](./glossary/booking-amount.md)
- [Discount Percentage](./glossary/discount-percentage.md)
- [Sales Order](./glossary/sales-order.md)
- [Customer Segment](./glossary/customer-segment.md)
- [Product Family](./glossary/product-family.md)
- [Technology Domain](./glossary/technology-domain.md)
- [Partner Type](./glossary/partner-type.md)
- [Route to Market](./glossary/route-to-market.md)
- [Fiscal Period](./glossary/fiscal-period.md)
- [Geography Region](./glossary/geography-region.md)

---

## Usage Instructions

This knowledge bundle is designed to be:
- **Human-readable**: Clear business documentation with context
- **Machine-readable**: Structured YAML frontmatter for automated processing
- **AI-searchable**: Semantic cross-links and rich metadata
- **Ontology-ready**: Compliant structure for OWL ontology generation

Navigate through the bundle using the index files in each folder or follow semantic cross-links between related concepts.

---

## Metadata

- **Version**: 0.1
- **Generated**: 2026-07-28T00:00:00Z
- **Source**: OSI Semantic Model - sales_bookings_and_revenue_analytics
- **Validation Status**: OKF Compliant
