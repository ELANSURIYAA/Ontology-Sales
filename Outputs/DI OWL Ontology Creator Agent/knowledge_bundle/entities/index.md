---
title: Entities Index
type: index
description: Catalog of business entities in the Sales Bookings and Revenue Analytics model
resource: entities
tags: [entities, index, business-entities, dimensions, facts]
timestamp: 2026-07-28T00:00:00Z
---

# Entities Index

## Overview

This index catalogs all business entities in the Sales Bookings and Revenue Analytics semantic model. Entities represent core business concepts including dimensions for analysis and fact tables containing transactional data and measures.

---

## Entity Catalog

### Dimensional Entities (7)

#### [Contract](contract.md)
**Entity ID**: ENT001  
**Technical Table**: QuoteToBooking.dim_contract  
**Business Keys**: Contract Key  
**Description**: Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level.

#### [Customer](customer.md)
**Entity ID**: ENT002  
**Technical Table**: QuoteToBooking.dim_customer  
**Business Keys**: Customer ID  
**Description**: Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location.

#### [Date](date.md)
**Entity ID**: ENT003  
**Technical Table**: QuoteToBooking.dim_date  
**Business Keys**: Date Key  
**Description**: Stores calendar and fiscal date attributes used to analyze bookings over time.

#### [Geography](geography.md)
**Entity ID**: ENT004  
**Technical Table**: QuoteToBooking.dim_geography  
**Business Keys**: Geography Key  
**Description**: Stores geographic attributes used to analyze bookings by sales region, theater, and country.

#### [Partner](partner.md)
**Entity ID**: ENT005  
**Technical Table**: QuoteToBooking.dim_partner  
**Business Keys**: Partner ID  
**Description**: Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market.

#### [Product](product.md)
**Entity ID**: ENT006  
**Technical Table**: QuoteToBooking.dim_product  
**Business Keys**: Product ID  
**Description**: Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity.

#### [Sales Representative](sales-representative.md)
**Entity ID**: ENT007  
**Technical Table**: QuoteToBooking.dim_sales_rep  
**Business Keys**: Sales Representative ID  
**Description**: Stores information about sales personnel responsible for managing customer relationships and booking transactions.

---

### Fact Entities (1)

#### [Booking Transaction](booking-transaction.md)
**Entity ID**: ENT008  
**Technical Table**: QuoteToBooking.fact_bookings  
**Business Keys**: Booking ID, Order Number, Order Line Number  
**Description**: Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions.

---

## Entity Relationships

### Star Schema Structure

```
                    Contract ──────┐
                                   │
    Customer ──────┐               │
                   │               │
    Date ──────────┤               │
                   │               │
    Geography ─────┼───► Booking Transaction
                   │               │
    Partner ───────┤               │
                   │               │
    Product ───────┘               │
                                   │
    Sales Representative ──────────┘
```

---

## Entity Statistics

| Category | Count |
|----------|-------|
| Total Entities | 8 |
| Dimensional Entities | 7 |
| Fact Entities | 1 |
| Total Attributes | 61 |
| Total Primary Keys | 8 |
| Total Foreign Keys | 7 |
| Total Measures | 6 |

---

## Entity Attributes Summary

| Entity | Attributes | Primary Key | Foreign Keys |
|--------|------------|-------------|--------------|
| Contract | 5 | Contract Key | 0 |
| Customer | 8 | Customer Key | 0 |
| Date | 7 | Date Key | 0 |
| Geography | 4 | Geography Key | 0 |
| Partner | 6 | Partner Key | 0 |
| Product | 7 | Product Key | 0 |
| Sales Representative | 6 | Sales Representative Key | 0 |
| Booking Transaction | 18 | Booking ID | 7 |

---

## Navigation

### By Entity Type
- [Dimensional Entities](#dimensional-entities-7)
- [Fact Entities](#fact-entities-1)

### Related Content
- [View All Domains](../domains/index.md)
- [View All Relationships](../relationships/index.md)
- [View All Measures](../measures/index.md)
- [View All Glossary Terms](../glossary/index.md)
- [View Semantic Summary](../semantic_summary.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Total Entities**: 8
**Source Schema**: QuoteToBooking
**Data Model Pattern**: Star Schema
**Last Updated**: 2026-07-28T00:00:00Z
**Format**: Open Knowledge Format (OKF)
