---
title: Sales Bookings and Revenue Analytics Knowledge Bundle
type: index
description: Complete semantic knowledge bundle for sales booking operations covering customers, products, partners, geographies, contracts, and revenue analytics
resource: knowledge_bundle
tags: [okf, bundle, sales, bookings, revenue, analytics, enterprise]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Bookings and Revenue Analytics Knowledge Bundle

## Overview

This knowledge bundle represents the complete semantic model for enterprise sales booking operations. It captures completed customer bookings and supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods.

---

## Bundle Structure

### [Semantic Summary](./semantic_summary.md)
High-level overview of the semantic model including domains, entities, relationships, and business context.

### [Metrics](./metrics.md)
Comprehensive catalog of business measures and KPIs used for sales performance analysis.

---

## Knowledge Components

### [Domains](./domains/index.md)
Business domains organizing the semantic model:
- [Sales Bookings and Revenue Analytics](./domains/sales-bookings-and-revenue-analytics.md)

### [Entities](./entities/index.md)
Core business entities in the model:
- [Contract](./entities/contract.md)
- [Customer](./entities/customer.md)
- [Date](./entities/date.md)
- [Geography](./entities/geography.md)
- [Partner](./entities/partner.md)
- [Product](./entities/product.md)
- [Sales Representative](./entities/sales-representative.md)
- [Booking Transaction](./entities/booking-transaction.md)

### [Relationships](./relationships/index.md)
Semantic relationships connecting entities:
- [Contract to Booking Transaction](./relationships/contract-to-booking-transaction.md)
- [Customer to Booking Transaction](./relationships/customer-to-booking-transaction.md)
- [Date to Booking Transaction](./relationships/date-to-booking-transaction.md)
- [Geography to Booking Transaction](./relationships/geography-to-booking-transaction.md)
- [Partner to Booking Transaction](./relationships/partner-to-booking-transaction.md)
- [Product to Booking Transaction](./relationships/product-to-booking-transaction.md)
- [Sales Representative to Booking Transaction](./relationships/sales-representative-to-booking-transaction.md)

### [Measures](./measures/index.md)
Business measures and financial metrics:
- [Quantity Sold](./measures/quantity-sold.md)
- [Unit List Price USD](./measures/unit-list-price-usd.md)
- [Discount Percentage](./measures/discount-percentage.md)
- [Booking Amount USD](./measures/booking-amount-usd.md)
- [Annual Contract Value USD](./measures/annual-contract-value-usd.md)
- [Total Contract Value USD](./measures/total-contract-value-usd.md)

### [Glossary](./glossary/index.md)
Business terminology and definitions (69 terms)

---

## Semantic Coverage

| Component | Count |
|-----------|-------|
| Domains | 1 |
| Entities | 8 |
| Attributes | 61 |
| Relationships | 7 |
| Measures | 6 |
| Glossary Terms | 69 |

---

## Usage

This knowledge bundle serves as the canonical semantic representation for:
- Business intelligence and analytics
- Data governance and stewardship
- Ontology development
- Semantic integration
- Business glossary management
- Metadata management

---

## Metadata

**Source**: OSI Semantic Model  
**Domain**: Sales Bookings and Revenue Analytics  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z  
**Format**: Open Knowledge Format (OKF)
