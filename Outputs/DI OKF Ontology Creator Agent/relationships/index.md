---
title: Relationships Index
type: index
description: Catalog of all entity relationships in the sales bookings and revenue analytics semantic model
resource: relationships
tags: [relationships, associations, connections, index]
timestamp: 2024-01-15T00:00:00Z
---

# Relationships Index

## Overview

This catalog contains all entity relationships defined in the sales bookings and revenue analytics semantic model. All relationships follow a many-to-one pattern from the Booking Transaction fact entity to dimension entities.

---

## Relationship Pattern

**Pattern**: Star Schema  
**Fact Entity**: Booking Transaction  
**Relationship Type**: Many-to-One

---

## Entity Relationships

### [Bookings to Contracts](bookings-to-contracts.md)
Links booking transactions to their associated contract terms and conditions.

**Source**: Booking Transaction  
**Target**: Contract  
**Type**: Many-to-One  
**Join Key**: contract_key

---

### [Bookings to Customers](bookings-to-customers.md)
Links booking transactions to the customer who placed the order.

**Source**: Booking Transaction  
**Target**: Customer  
**Type**: Many-to-One  
**Join Key**: customer_key

---

### [Bookings to Dates](bookings-to-dates.md)
Links booking transactions to the date when the booking occurred.

**Source**: Booking Transaction  
**Target**: Date  
**Type**: Many-to-One  
**Join Key**: date_key

---

### [Bookings to Geographies](bookings-to-geographies.md)
Links booking transactions to the geographic territory where the sale occurred.

**Source**: Booking Transaction  
**Target**: Geography  
**Type**: Many-to-One  
**Join Key**: geography_key

---

### [Bookings to Partners](bookings-to-partners.md)
Links booking transactions to the partner involved in fulfilling the sale.

**Source**: Booking Transaction  
**Target**: Partner  
**Type**: Many-to-One  
**Join Key**: partner_key

---

### [Bookings to Products](bookings-to-products.md)
Links booking transactions to the product or offer that was sold.

**Source**: Booking Transaction  
**Target**: Product  
**Type**: Many-to-One  
**Join Key**: product_key

---

### [Bookings to Sales Representatives](bookings-to-sales-representatives.md)
Links booking transactions to the sales representative who closed the deal.

**Source**: Booking Transaction  
**Target**: Sales Representative  
**Type**: Many-to-One  
**Join Key**: sales_rep_key

---

## Relationship Summary

| Relationship | Source | Target | Cardinality | Join Key |
|--------------|--------|--------|-------------|----------|
| Bookings to Contracts | Booking Transaction | Contract | Many-to-One | contract_key |
| Bookings to Customers | Booking Transaction | Customer | Many-to-One | customer_key |
| Bookings to Dates | Booking Transaction | Date | Many-to-One | date_key |
| Bookings to Geographies | Booking Transaction | Geography | Many-to-One | geography_key |
| Bookings to Partners | Booking Transaction | Partner | Many-to-One | partner_key |
| Bookings to Products | Booking Transaction | Product | Many-to-One | product_key |
| Bookings to Sales Representatives | Booking Transaction | Sales Representative | Many-to-One | sales_rep_key |

---

## Navigation

- [Return to Index](../index.md)
- [View Semantic Summary](../semantic_summary.md)
- [View All Entities](../entities/index.md)
- [View All Domains](../domains/index.md)
