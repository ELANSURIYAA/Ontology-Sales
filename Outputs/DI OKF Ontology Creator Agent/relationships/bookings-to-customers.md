---
title: Bookings to Customers
type: relationship
description: Links booking transactions to the customer who placed the order
resource: relationships
tags: [bookings, customers, relationship, many-to-one]
timestamp: 2024-01-15T00:00:00Z
---

# Bookings to Customers

## Business Definition

This relationship links booking transactions to the customer who placed the order, enabling analysis of bookings by customer segment, industry, account tier, and headquarters location.

---

## Relationship Details

**Source Entity**: [Booking Transaction](../entities/bookings.md)  
**Target Entity**: [Customer](../entities/customers.md)  
**Relationship Type**: Many-to-One  
**Cardinality**: Many bookings can be associated with one customer

---

## Technical Mapping

**Join Type**: Inner Join  
**Left Key**: bookings.customer_key  
**Right Key**: customers.customer_key

---

## Business Description

Each booking transaction is associated with a specific customer organization that placed the order. Customer attributes include segment classification (Enterprise, Service Provider, Public Sector), industry vertical, account tier (strategic importance), and headquarters location (country and region). Multiple booking transactions can be associated with the same customer.

---

## Usage

This relationship enables analysis such as:

- Bookings by customer segment
- Industry vertical performance
- Account tier revenue contribution
- Customer-level booking trends
- Geographic customer distribution

---

## Related Concepts

- [Customer Segment](../glossary/customer-segment.md)
- [Industry](../glossary/industry.md)
- [Account Tier](../glossary/account-tier.md)
- [Headquarters Country](../glossary/hq-country.md)
- [Headquarters Region](../glossary/hq-region.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Customer Entity](../entities/customers.md)
- [View Customers Domain](../domains/customers.md)
