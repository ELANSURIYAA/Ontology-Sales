---
title: Entities Index
type: index
description: Index of all business entities in the sales bookings and revenue analytics semantic model
resource: entities
tags: [entities, index, datasets]
timestamp: 2026-07-28T00:00:00Z
---

# Entities Index

## Overview

This index contains all business entities (datasets) defined in the semantic model.

---

## Fact Entity

### [Bookings](bookings.md)
Captures individual completed sales booking transactions and their associated financial measures, quantities, renewal status, and links to related business dimensions.

**Source**: quotetobooking.fact_bookings

**Primary Key**: booking_id

---

## Dimension Entities

### [Customers](customers.md)
Stores descriptive information about customers that place orders, including identity, segment, industry, account tier, and headquarters location.

**Source**: quotetobooking.dim_customer

**Primary Key**: customer_key

---

### [Products](products.md)
Stores descriptive information about products and offers sold to customers, including product identity, family, technology domain, offer type, and business entity.

**Source**: quotetobooking.dim_product

**Primary Key**: product_key

---

### [Partners](partners.md)
Stores information about direct and indirect sales partners involved in fulfilling customer bookings, including partner identity, type, tier, and route to market.

**Source**: quotetobooking.dim_partner

**Primary Key**: partner_key

---

### [Geographies](geographies.md)
Stores geographic sales territory attributes used to analyze bookings by region, theater, and country.

**Source**: quotetobooking.dim_geography

**Primary Key**: geography_key

---

### [Sales Representatives](sales-representatives.md)
Stores information about the sales person responsible for managing customer relationships and booking transactions, including role, team, and segment coverage.

**Source**: quotetobooking.dim_sales_rep

**Primary Key**: sales_rep_key

---

### [Contracts](contracts.md)
Describes the commercial agreement or service coverage terms associated with a booking, including contract type, duration, renewal behavior, and support coverage level.

**Source**: quotetobooking.dim_contract

**Primary Key**: contract_key

---

### [Dates](dates.md)
Provides calendar and fiscal time attributes used to analyze bookings across reporting periods, years, quarters, and months.

**Source**: quotetobooking.dim_date

**Primary Key**: date_key

---

## Navigation

- [Return to Index](../index.md)
- [View Semantic Summary](../semantic_summary.md)
- [Browse Domains](../domains/index.md)
- [Browse Relationships](../relationships/index.md)
- [Browse Measures](../measures/index.md)
- [Browse Glossary](../glossary/index.md)
