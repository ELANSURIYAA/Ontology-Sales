---
title: Entities Index
type: index
description: Index of all business entities in the sales bookings and revenue analytics semantic model
resource: entities
tags: [entities, business-entities, index]
timestamp: 2026-07-28T00:00:00Z
---

# Business Entities Index

## Overview

This index provides access to all business entities defined in the sales bookings and revenue analytics semantic model. Entities represent the core business objects and dimensions used for analysis.

---

## Entity Categories

### Fact Entities
Core transactional entities capturing business events

### Dimension Entities
Descriptive entities providing context for analysis

---

## Fact Entities

### [Bookings](./bookings.md)
**Description**: Captures individual completed sales booking transactions and their associated financial measures, quantities, renewal status, and links to related business dimensions

**Source**: quotetobooking.fact_bookings

**Primary Key**: booking_id

**Related Domain**: [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Dimension Entities

### [Customers](./customers.md)
**Description**: Stores descriptive information about customers that place orders, including identity, segment, industry, account tier, and headquarters location

**Source**: quotetobooking.dim_customer

**Primary Key**: customer_key

**Related Domain**: [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

### [Products](./products.md)
**Description**: Stores descriptive information about products and offers sold to customers, including product identity, family, technology domain, offer type, and business entity

**Source**: quotetobooking.dim_product

**Primary Key**: product_key

**Related Domain**: [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

### [Partners](./partners.md)
**Description**: Stores information about direct and indirect sales partners involved in fulfilling customer bookings, including partner identity, type, tier, and route to market

**Source**: quotetobooking.dim_partner

**Primary Key**: partner_key

**Related Domain**: [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

### [Geographies](./geographies.md)
**Description**: Stores geographic sales territory attributes used to analyze bookings by region, theater, and country

**Source**: quotetobooking.dim_geography

**Primary Key**: geography_key

**Related Domain**: [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

### [Sales Representatives](./sales-representatives.md)
**Description**: Stores information about the sales person responsible for managing customer relationships and booking transactions, including role, team, and segment coverage

**Source**: quotetobooking.dim_sales_rep

**Primary Key**: sales_rep_key

**Related Domain**: [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

### [Contracts](./contracts.md)
**Description**: Describes the commercial agreement or service coverage terms associated with a booking, including contract type, duration, renewal behavior, and support coverage level

**Source**: quotetobooking.dim_contract

**Primary Key**: contract_key

**Related Domain**: [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

### [Dates](./dates.md)
**Description**: Provides calendar and fiscal time attributes used to analyze bookings across reporting periods, years, quarters, and months

**Source**: quotetobooking.dim_date

**Primary Key**: date_key

**Related Domain**: [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Entity Count

**Total Entities**: 8
- **Fact Entities**: 1
- **Dimension Entities**: 7

---

## Entity Relationships

All dimension entities are connected to the Bookings fact entity through many-to-one relationships:

- [Bookings to Contracts](../relationships/bookings-to-contracts.md)
- [Bookings to Customers](../relationships/bookings-to-customers.md)
- [Bookings to Dates](../relationships/bookings-to-dates.md)
- [Bookings to Geographies](../relationships/bookings-to-geographies.md)
- [Bookings to Partners](../relationships/bookings-to-partners.md)
- [Bookings to Products](../relationships/bookings-to-products.md)
- [Bookings to Sales Representatives](../relationships/bookings-to-sales-representatives.md)

---

## Navigation

- [Back to Knowledge Bundle Index](../index.md)
- [Semantic Summary](../semantic_summary.md)
- [Domains Index](../domains/index.md)
- [Relationships Index](../relationships/index.md)
- [Measures Index](../measures/index.md)
- [Glossary Index](../glossary/index.md)
