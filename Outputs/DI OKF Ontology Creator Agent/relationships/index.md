---
title: Relationships Index
type: index
description: Index of all relationships in the sales bookings and revenue analytics semantic model
resource: relationships
tags: [relationships, index, joins]
timestamp: 2026-07-28T00:00:00Z
---

# Relationships Index

## Overview

This index contains all relationships defined in the semantic model. The model follows a star schema pattern with Bookings as the central fact entity.

---

## Fact to Dimension Relationships

### [Bookings to Contracts](bookings-to-contracts.md)
Links booking transactions to contract terms and service coverage.

**Type**: many-to-one

**Source**: [Bookings](../entities/bookings.md)

**Target**: [Contracts](../entities/contracts.md)

---

### [Bookings to Customers](bookings-to-customers.md)
Links booking transactions to customer organizations.

**Type**: many-to-one

**Source**: [Bookings](../entities/bookings.md)

**Target**: [Customers](../entities/customers.md)

---

### [Bookings to Dates](bookings-to-dates.md)
Links booking transactions to calendar and fiscal time periods.

**Type**: many-to-one

**Source**: [Bookings](../entities/bookings.md)

**Target**: [Dates](../entities/dates.md)

---

### [Bookings to Geographies](bookings-to-geographies.md)
Links booking transactions to geographic sales territories.

**Type**: many-to-one

**Source**: [Bookings](../entities/bookings.md)

**Target**: [Geographies](../entities/geographies.md)

---

### [Bookings to Partners](bookings-to-partners.md)
Links booking transactions to sales partners and channels.

**Type**: many-to-one

**Source**: [Bookings](../entities/bookings.md)

**Target**: [Partners](../entities/partners.md)

---

### [Bookings to Products](bookings-to-products.md)
Links booking transactions to products and offers.

**Type**: many-to-one

**Source**: [Bookings](../entities/bookings.md)

**Target**: [Products](../entities/products.md)

---

### [Bookings to Sales Representatives](bookings-to-sales-representatives.md)
Links booking transactions to sales personnel.

**Type**: many-to-one

**Source**: [Bookings](../entities/bookings.md)

**Target**: [Sales Representatives](../entities/sales-representatives.md)

---

## Navigation

- [Return to Index](../index.md)
- [View Semantic Summary](../semantic_summary.md)
- [Browse Domains](../domains/index.md)
- [Browse Entities](../entities/index.md)
- [Browse Measures](../measures/index.md)
- [Browse Glossary](../glossary/index.md)
