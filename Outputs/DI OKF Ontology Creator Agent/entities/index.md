---
title: Entities Index
type: index
description: Catalog of all business entities in the sales bookings and revenue analytics semantic model
resource: entities
tags: [entities, catalog, index, business-objects]
timestamp: 2024-01-15T00:00:00Z
---

# Entities Index

## Overview

This catalog contains all business entities defined in the sales bookings and revenue analytics semantic model. Each entity represents a core business object with attributes, relationships, and measures.

---

## Business Entities

### [Booking Transaction](bookings.md)
Individual completed sales booking transactions with financial measures, quantities, renewal status, and dimensional links.

**Type**: Fact Entity  
**Primary Key**: booking_id  
**Source**: quotetobooking.fact_bookings

---

### [Customer](customers.md)
Customer organizations that place orders, including identity, segment, industry, account tier, and headquarters location.

**Type**: Dimension Entity  
**Primary Key**: customer_key  
**Source**: quotetobooking.dim_customer

---

### [Product](products.md)
Products and offers sold to customers, including product identity, family, technology domain, offer type, and business entity.

**Type**: Dimension Entity  
**Primary Key**: product_key  
**Source**: quotetobooking.dim_product

---

### [Partner](partners.md)
Direct and indirect sales partners involved in fulfilling customer bookings, including partner identity, type, tier, and route to market.

**Type**: Dimension Entity  
**Primary Key**: partner_key  
**Source**: quotetobooking.dim_partner

---

### [Geography](geographies.md)
Geographic sales territory attributes used to analyze bookings by region, theater, and country.

**Type**: Dimension Entity  
**Primary Key**: geography_key  
**Source**: quotetobooking.dim_geography

---

### [Sales Representative](sales-representatives.md)
Sales persons responsible for managing customer relationships and booking transactions, including role, team, and segment coverage.

**Type**: Dimension Entity  
**Primary Key**: sales_rep_key  
**Source**: quotetobooking.dim_sales_rep

---

### [Contract](contracts.md)
Commercial agreement or service coverage terms associated with bookings, including contract type, duration, renewal behavior, and support coverage level.

**Type**: Dimension Entity  
**Primary Key**: contract_key  
**Source**: quotetobooking.dim_contract

---

### [Date](dates.md)
Calendar and fiscal time attributes used to analyze bookings across reporting periods, years, quarters, and months.

**Type**: Dimension Entity  
**Primary Key**: date_key  
**Source**: quotetobooking.dim_date

---

## Entity Summary

| Entity | Type | Attributes | Relationships | Domain |
|--------|------|------------|---------------|--------|
| Booking Transaction | Fact | 17 | 7 | Bookings |
| Customer | Dimension | 7 | 1 | Customers |
| Product | Dimension | 7 | 1 | Products |
| Partner | Dimension | 6 | 1 | Partners |
| Geography | Dimension | 4 | 1 | Geographies |
| Sales Representative | Dimension | 6 | 1 | Sales Representatives |
| Contract | Dimension | 5 | 1 | Contracts |
| Date | Dimension | 7 | 1 | Dates |

---

## Navigation

- [Return to Index](../index.md)
- [View Semantic Summary](../semantic_summary.md)
- [View All Domains](../domains/index.md)
- [View All Relationships](../relationships/index.md)
- [View All Measures](../measures/index.md)
