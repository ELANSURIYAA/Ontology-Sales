---
title: Entities Index
type: index
description: Navigation index for business entities
resource: entities
tags: [entities, index, business-entity]
timestamp: 2026-07-28T00:00:00Z
---

# Entities Index

This index provides navigation to all business entity documents in the knowledge bundle.

---

## Entity Overview

The knowledge bundle contains **8** business entities:
- **7** Dimension Entities
- **1** Fact Entity

---

## Dimension Entities

### [Contract](contract.md)
Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level.

**Technical Table**: QuoteToBooking.dim_contract  
**Primary Key**: Contract Key

---

### [Customer](customer.md)
Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location.

**Technical Table**: QuoteToBooking.dim_customer  
**Primary Key**: Customer Key

---

### [Date](date.md)
Stores calendar and fiscal date attributes used to analyze bookings over time.

**Technical Table**: QuoteToBooking.dim_date  
**Primary Key**: Date Key

---

### [Geography](geography.md)
Stores geographic attributes used to analyze bookings by sales region, theater, and country.

**Technical Table**: QuoteToBooking.dim_geography  
**Primary Key**: Geography Key

---

### [Partner](partner.md)
Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market.

**Technical Table**: QuoteToBooking.dim_partner  
**Primary Key**: Partner Key

---

### [Product](product.md)
Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity.

**Technical Table**: QuoteToBooking.dim_product  
**Primary Key**: Product Key

---

### [Sales Representative](sales-representative.md)
Stores information about sales personnel responsible for managing customer relationships and booking transactions.

**Technical Table**: QuoteToBooking.dim_sales_rep  
**Primary Key**: Sales Representative Key

---

## Fact Entities

### [Booking Transaction](booking-transaction.md)
Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions.

**Technical Table**: QuoteToBooking.fact_bookings  
**Primary Keys**: Booking ID, Order Number, Order Line Number

---

## Entity Relationships

All dimension entities have a **One-to-Many** relationship with the Booking Transaction fact entity:

- [Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)
- [Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)
- [Date to Booking Transaction](../relationships/date-to-booking-transaction.md)
- [Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)
- [Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)
- [Product to Booking Transaction](../relationships/product-to-booking-transaction.md)
- [Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)

---

## Navigation

- [Back to Index](../index.md)
- [Semantic Summary](../semantic_summary.md)
- [View Domains](../domains/index.md)
- [View Relationships](../relationships/index.md)
- [View Measures](../measures/index.md)
- [View Glossary](../glossary/index.md)
