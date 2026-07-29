---
title: Entities Index
type: index
description: Complete catalog of business entities in the Sales Bookings and Revenue Analytics knowledge bundle
resource: entities
tags: [entities, index, catalog]
timestamp: 2026-07-28T00:00:00Z
---

# Entities Index

## Overview

This index catalogs all business entities in the Sales Bookings and Revenue Analytics knowledge bundle. Entities represent core business concepts with attributes, relationships, and measures.

---

## Entity Catalog

### Dimensional Entities

#### [Contract](./contract.md)
**Entity ID:** ENT001  
**Technical Table:** QuoteToBooking.dim_contract  
**Description:** Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level.

#### [Customer](./customer.md)
**Entity ID:** ENT002  
**Technical Table:** QuoteToBooking.dim_customer  
**Description:** Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location.

#### [Date](./date.md)
**Entity ID:** ENT003  
**Technical Table:** QuoteToBooking.dim_date  
**Description:** Stores calendar and fiscal date attributes used to analyze bookings over time.

#### [Geography](./geography.md)
**Entity ID:** ENT004  
**Technical Table:** QuoteToBooking.dim_geography  
**Description:** Stores geographic attributes used to analyze bookings by sales region, theater, and country.

#### [Partner](./partner.md)
**Entity ID:** ENT005  
**Technical Table:** QuoteToBooking.dim_partner  
**Description:** Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market.

#### [Product](./product.md)
**Entity ID:** ENT006  
**Technical Table:** QuoteToBooking.dim_product  
**Description:** Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity.

#### [Sales Representative](./sales-representative.md)
**Entity ID:** ENT007  
**Technical Table:** QuoteToBooking.dim_sales_rep  
**Description:** Stores information about sales personnel responsible for managing customer relationships and booking transactions.

---

### Fact Entities

#### [Booking Transaction](./booking-transaction.md)
**Entity ID:** ENT008  
**Technical Table:** QuoteToBooking.fact_bookings  
**Description:** Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions.

---

## Entity Statistics

- **Total Entities:** 8
- **Dimensional Entities:** 7
- **Fact Entities:** 1
- **Total Attributes:** 61
- **Total Relationships:** 7

---

## Entity Relationships

All dimensional entities connect to the central **Booking Transaction** fact entity through foreign key relationships:

- Contract → Booking Transaction
- Customer → Booking Transaction
- Date → Booking Transaction
- Geography → Booking Transaction
- Partner → Booking Transaction
- Product → Booking Transaction
- Sales Representative → Booking Transaction

---

## Navigation

- [Return to Bundle Index](../index.md)
- [View Semantic Summary](../semantic_summary.md)
- [View All Domains](../domains/index.md)
- [View All Relationships](../relationships/index.md)
- [View All Measures](../measures/index.md)
