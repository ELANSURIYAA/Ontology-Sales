---
title: Entities Index
type: index
description: Navigation index for all business entities in the Quote to Booking semantic model
resource: entities
tags: [okf, entities, index, quote-to-booking]
timestamp: 2026-07-28T00:00:00Z
---

# Business Entities Index

## Overview

This index provides navigation to all business entities within the Quote to Booking semantic model. The model follows a star schema pattern with 7 dimension entities and 1 fact entity.

---

## Entity Catalog

### Dimension Entities

#### [Contract Dimension](contract-dimension.md)
**Entity ID**: ENT001  
**Domain**: Contract Management  
**Technical Table**: quotetobooking.dim_contract  
**Description**: Stores contract and service agreement attributes used to classify bookings by contract type, term, renewal behavior, and coverage level.  
**Business Keys**: Contract Key

---

#### [Customer Dimension](customer-dimension.md)
**Entity ID**: ENT002  
**Domain**: Customer Management  
**Technical Table**: quotetobooking.dim_customer  
**Description**: Stores descriptive customer attributes used to analyze bookings by customer identity, segment, industry, account tier, and headquarters location.  
**Business Keys**: Customer Key, Customer ID

---

#### [Date Dimension](date-dimension.md)
**Entity ID**: ENT003  
**Domain**: Time Management  
**Technical Table**: quotetobooking.dim_date  
**Description**: Stores calendar and fiscal date attributes used to analyze bookings across time periods, fiscal years, quarters, and months.  
**Business Keys**: Date Key, Full Date

---

#### [Geography Dimension](geography-dimension.md)
**Entity ID**: ENT004  
**Domain**: Geography  
**Technical Table**: quotetobooking.dim_geography  
**Description**: Stores geographic attributes used to analyze bookings by region, theater, and country.  
**Business Keys**: Geography Key

---

#### [Partner Dimension](partner-dimension.md)
**Entity ID**: ENT005  
**Domain**: Partner Management  
**Technical Table**: quotetobooking.dim_partner  
**Description**: Stores channel partner attributes used to analyze bookings by partner identity, partner type, partner tier, and route to market.  
**Business Keys**: Partner Key, Partner ID

---

#### [Product Dimension](product-dimension.md)
**Entity ID**: ENT006  
**Domain**: Product Management  
**Technical Table**: quotetobooking.dim_product  
**Description**: Stores product and offer attributes used to analyze bookings by product identity, family, technology domain, offer type, and business entity.  
**Business Keys**: Product Key, Product ID

---

#### [Sales Representative Dimension](sales-representative-dimension.md)
**Entity ID**: ENT007  
**Domain**: Sales Organization  
**Technical Table**: quotetobooking.dim_sales_rep  
**Description**: Stores sales representative attributes used to analyze bookings by sales person, role, team, and market segment coverage.  
**Business Keys**: Sales Representative Key, Sales Representative ID

---

### Fact Entities

#### [Booking Fact](booking-fact.md)
**Entity ID**: ENT008  
**Domain**: Sales Transactions  
**Technical Table**: quotetobooking.fact_bookings  
**Description**: Stores individual booking transactions and their financial measures for analyzing sales performance across customers, products, partners, geographies, contracts, sales representatives, and time.  
**Business Keys**: Booking ID, Order Number, Order Line Number

---

## Entity Statistics

- **Total Entities**: 8
- **Dimension Entities**: 7
- **Fact Entities**: 1
- **Total Attributes**: 61
- **Total Relationships**: 7

---

## Entity Relationships

### Star Schema Pattern

The model implements a star schema with the Booking Fact at the center connected to 7 dimension entities:

```
Contract Dimension ──┐
Customer Dimension ──┤
Date Dimension ──────┤
Geography Dimension ─┤──→ Booking Fact
Partner Dimension ───┤
Product Dimension ───┤
Sales Rep Dimension ─┘
```

All relationships are one-to-many from dimension to fact.

---

## Entity Types

### Master Data Entities
- Contract Dimension
- Customer Dimension
- Date Dimension
- Geography Dimension
- Partner Dimension
- Product Dimension
- Sales Representative Dimension

### Transactional Entities
- Booking Fact

---

## Navigation

- [Back to Bundle Index](../index.md)
- [Semantic Summary](../semantic_summary.md)
- [Domains Index](../domains/index.md)
- [Relationships Index](../relationships/index.md)
- [Measures Index](../measures/index.md)
- [Glossary Index](../glossary/index.md)
