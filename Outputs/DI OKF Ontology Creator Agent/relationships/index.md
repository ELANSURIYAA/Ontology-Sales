---
title: Relationships Index
type: index
description: Index of all business relationships in the sales bookings and revenue analytics semantic model
resource: relationships
tags: [relationships, business-relationships, index]
timestamp: 2026-07-28T00:00:00Z
---

# Business Relationships Index

## Overview

This index provides access to all business relationships defined in the sales bookings and revenue analytics semantic model. Relationships define how entities are connected and enable dimensional analysis of booking transactions.

---

## Relationship Pattern

All relationships in this model follow a **star schema pattern** where the Bookings fact table is connected to dimension tables through many-to-one relationships.

---

## Relationship List

### [Bookings to Contracts](./bookings-to-contracts.md)
**Type**: Many-to-one

**Description**: Links booking transactions to contract terms and conditions

**Source Entity**: [Bookings](../entities/bookings.md)

**Target Entity**: [Contracts](../entities/contracts.md)

**Join Key**: contract_key

---

### [Bookings to Customers](./bookings-to-customers.md)
**Type**: Many-to-one

**Description**: Links booking transactions to customer accounts

**Source Entity**: [Bookings](../entities/bookings.md)

**Target Entity**: [Customers](../entities/customers.md)

**Join Key**: customer_key

---

### [Bookings to Dates](./bookings-to-dates.md)
**Type**: Many-to-one

**Description**: Links booking transactions to time periods

**Source Entity**: [Bookings](../entities/bookings.md)

**Target Entity**: [Dates](../entities/dates.md)

**Join Key**: date_key

---

### [Bookings to Geographies](./bookings-to-geographies.md)
**Type**: Many-to-one

**Description**: Links booking transactions to geographic territories

**Source Entity**: [Bookings](../entities/bookings.md)

**Target Entity**: [Geographies](../entities/geographies.md)

**Join Key**: geography_key

---

### [Bookings to Partners](./bookings-to-partners.md)
**Type**: Many-to-one

**Description**: Links booking transactions to sales partners

**Source Entity**: [Bookings](../entities/bookings.md)

**Target Entity**: [Partners](../entities/partners.md)

**Join Key**: partner_key

---

### [Bookings to Products](./bookings-to-products.md)
**Type**: Many-to-one

**Description**: Links booking transactions to products

**Source Entity**: [Bookings](../entities/bookings.md)

**Target Entity**: [Products](../entities/products.md)

**Join Key**: product_key

---

### [Bookings to Sales Representatives](./bookings-to-sales-representatives.md)
**Type**: Many-to-one

**Description**: Links booking transactions to sales representatives

**Source Entity**: [Bookings](../entities/bookings.md)

**Target Entity**: [Sales Representatives](../entities/sales-representatives.md)

**Join Key**: sales_rep_key

---

## Relationship Count

**Total Relationships**: 7

**Relationship Type**: Many-to-one (all)

---

## Cardinality Rules

### Many-to-One Relationships
- Multiple booking transactions can reference the same dimension record
- Each booking transaction references exactly one record in each dimension table
- Dimension records can exist without associated bookings (optional relationship)

---

## Referential Integrity

All relationships enforce referential integrity:
- Foreign keys in the Bookings fact table must reference valid primary keys in dimension tables
- Dimension records can be added independently of bookings
- Bookings cannot be created without valid dimension references

---

## Navigation

- [Back to Knowledge Bundle Index](../index.md)
- [Semantic Summary](../semantic_summary.md)
- [Domains Index](../domains/index.md)
- [Entities Index](../entities/index.md)
- [Measures Index](../measures/index.md)
- [Glossary Index](../glossary/index.md)
