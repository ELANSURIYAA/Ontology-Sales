---
title: Domains Index
type: index
description: Navigation index for all business domains in the Quote to Booking semantic model
resource: domains
tags: [okf, domains, index, quote-to-booking]
timestamp: 2026-07-28T00:00:00Z
---

# Business Domains Index

## Overview

This index provides navigation to all business domains within the Quote to Booking semantic model. Each domain represents a distinct area of business knowledge with associated entities, measures, and relationships.

---

## Domain Catalog

### [Sales Transactions](sales-transactions.md)
**Domain ID**: DOM001  
**Description**: Completed customer booking transactions and associated sales performance measures across orders, renewals, quantities, pricing, and revenue values.  
**Related Entities**: Booking Fact  
**Related Measures**: Quantity Sold, Unit List Price USD, Discount Percentage, Booking Amount USD, Annual Contract Value USD, Total Contract Value USD

---

### [Customer Management](customer-management.md)
**Domain ID**: DOM002  
**Description**: Customer master data used to analyze bookings by customer identity, segment, industry, account tier, and headquarters location.  
**Related Entities**: Customer Dimension  
**Related Measures**: All revenue and volume measures by customer

---

### [Product Management](product-management.md)
**Domain ID**: DOM003  
**Description**: Product and offer master data used to analyze bookings by product identity, family, technology domain, offer type, and business entity.  
**Related Entities**: Product Dimension  
**Related Measures**: All revenue and volume measures by product

---

### [Partner Management](partner-management.md)
**Domain ID**: DOM004  
**Description**: Channel partner master data used to analyze bookings by partner identity, type, tier, and route to market.  
**Related Entities**: Partner Dimension  
**Related Measures**: All revenue and volume measures by partner

---

### [Geography](geography.md)
**Domain ID**: DOM005  
**Description**: Geographic master data used to analyze bookings by region, theater, and country.  
**Related Entities**: Geography Dimension  
**Related Measures**: All revenue and volume measures by geography

---

### [Sales Organization](sales-organization.md)
**Domain ID**: DOM006  
**Description**: Sales representative and organizational attributes used to analyze bookings by seller, role, team, and covered segment.  
**Related Entities**: Sales Representative Dimension  
**Related Measures**: All revenue and volume measures by sales representative

---

### [Contract Management](contract-management.md)
**Domain ID**: DOM007  
**Description**: Contract and service agreement attributes used to classify bookings by contract type, term, renewal behavior, and coverage level.  
**Related Entities**: Contract Dimension  
**Related Measures**: All revenue and volume measures by contract

---

### [Time Management](time-management.md)
**Domain ID**: DOM008  
**Description**: Calendar and fiscal time attributes used to analyze bookings across dates, months, years, quarters, and fiscal periods.  
**Related Entities**: Date Dimension  
**Related Measures**: All revenue and volume measures by time period

---

### [Pricing](pricing.md)
**Domain ID**: DOM009  
**Description**: Pricing attributes used to analyze unit list price and discount characteristics of booked transactions.  
**Related Entities**: Booking Fact  
**Related Measures**: Unit List Price USD, Discount Percentage

---

### [Revenue Metrics](revenue-metrics.md)
**Domain ID**: DOM010  
**Description**: Financial value attributes used to analyze booked revenue, annual contract value, and total contract value.  
**Related Entities**: Booking Fact  
**Related Measures**: Booking Amount USD, Annual Contract Value USD, Total Contract Value USD

---

## Domain Statistics

- **Total Domains**: 10
- **Transactional Domains**: 2 (Sales Transactions, Contract Management)
- **Master Data Domains**: 5 (Customer, Product, Partner, Geography, Sales Organization)
- **Analytical Domains**: 3 (Time Management, Pricing, Revenue Metrics)

---

## Domain Relationships

### Master Data to Transactions
All master data domains (Customer, Product, Partner, Geography, Sales Organization, Contract, Time) provide dimensional context for analyzing Sales Transactions.

### Analytical Domains
Pricing and Revenue Metrics domains provide specialized analytical perspectives on Sales Transactions.

---

## Navigation

- [Back to Bundle Index](../index.md)
- [Semantic Summary](../semantic_summary.md)
- [Entities Index](../entities/index.md)
- [Relationships Index](../relationships/index.md)
- [Measures Index](../measures/index.md)
- [Glossary Index](../glossary/index.md)
