---
title: Entity Index
type: index
description: Catalog of business entities in the Sales Bookings and Revenue Analytics semantic model
resource: entities
tags: [entities, business, catalog, index]
timestamp: 2026-07-28T00:00:00Z
---

# Entity Index

## Overview

This index catalogs all business entities in the semantic model. Entities represent core business concepts including dimensions and facts that form the foundation of the analytical model.

---

## Entity Catalog

### Dimension Entities

#### [Contract](./contract.md)
**Entity ID**: ENT001  
**Description**: Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level.  
**Technical Table**: QuoteToBooking.dim_contract  
**Primary Key**: Contract Key

#### [Customer](./customer.md)
**Entity ID**: ENT002  
**Description**: Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location.  
**Technical Table**: QuoteToBooking.dim_customer  
**Primary Key**: Customer Key

#### [Date](./date.md)
**Entity ID**: ENT003  
**Description**: Stores calendar and fiscal date attributes used to analyze bookings over time.  
**Technical Table**: QuoteToBooking.dim_date  
**Primary Key**: Date Key

#### [Geography](./geography.md)
**Entity ID**: ENT004  
**Description**: Stores geographic attributes used to analyze bookings by sales region, theater, and country.  
**Technical Table**: QuoteToBooking.dim_geography  
**Primary Key**: Geography Key

#### [Partner](./partner.md)
**Entity ID**: ENT005  
**Description**: Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market.  
**Technical Table**: QuoteToBooking.dim_partner  
**Primary Key**: Partner Key

#### [Product](./product.md)
**Entity ID**: ENT006  
**Description**: Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity.  
**Technical Table**: QuoteToBooking.dim_product  
**Primary Key**: Product Key

#### [Sales Representative](./sales-representative.md)
**Entity ID**: ENT007  
**Description**: Stores information about sales personnel responsible for managing customer relationships and booking transactions.  
**Technical Table**: QuoteToBooking.dim_sales_rep  
**Primary Key**: Sales Representative Key

---

### Fact Entities

#### [Booking Transaction](./booking-transaction.md)
**Entity ID**: ENT008  
**Description**: Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions.  
**Technical Table**: QuoteToBooking.fact_bookings  
**Primary Keys**: Booking ID, Order Number, Order Line Number

---

## Entity Statistics

| Metric | Count |
|--------|-------|
| Total Entities | 8 |
| Dimension Entities | 7 |
| Fact Entities | 1 |
| Total Attributes | 61 |
| Primary Keys | 8 |
| Foreign Keys | 7 |

---

## Entity Relationships

All dimension entities have one-to-many relationships with the Booking Transaction fact entity:

- Contract → Booking Transaction
- Customer → Booking Transaction
- Date → Booking Transaction
- Geography → Booking Transaction
- Partner → Booking Transaction
- Product → Booking Transaction
- Sales Representative → Booking Transaction

See [Relationship Index](../relationships/index.md) for detailed relationship documentation.

---

## Semantic Links

- [Main Index](../index.md)
- [Semantic Summary](../semantic_summary.md)
- [Domain Index](../domains/index.md)
- [Relationship Index](../relationships/index.md)
- [Measure Index](../measures/index.md)
- [Glossary Index](../glossary/index.md)

---

## Metadata

**Resource Type**: Entity Catalog  
**Total Entities**: 8  
**Domain**: Sales Bookings and Revenue Analytics  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
