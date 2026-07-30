---
title: Bookings to Sales Representatives
type: relationship
description: Links booking transactions to the sales representative who closed the deal
resource: relationships
tags: [bookings, sales-representatives, relationship, many-to-one]
timestamp: 2024-01-15T00:00:00Z
---

# Bookings to Sales Representatives

## Business Definition

This relationship links booking transactions to the sales representative who closed the deal, enabling analysis of bookings by sales role, sales team, and segment coverage.

---

## Relationship Details

**Source Entity**: [Booking Transaction](../entities/bookings.md)  
**Target Entity**: [Sales Representative](../entities/sales-representatives.md)  
**Relationship Type**: Many-to-One  
**Cardinality**: Many bookings can be associated with one sales representative

---

## Technical Mapping

**Join Type**: Inner Join  
**Left Key**: bookings.sales_rep_key  
**Right Key**: sales_representatives.sales_rep_key

---

## Business Description

Each booking transaction is associated with a specific sales representative who closed the deal and manages the customer relationship. Sales representative attributes include sales role (Account Executive, Sales Engineer), sales team (organizational unit), and segment covered (customer segment assignment). Multiple booking transactions can be associated with the same sales representative.

---

## Usage

This relationship enables analysis such as:

- Individual sales representative performance
- Sales team effectiveness
- Role-based performance comparison
- Segment coverage analysis
- Quota attainment tracking

---

## Related Concepts

- [Sales Role](../glossary/sales-role.md)
- [Sales Team](../glossary/sales-team.md)
- [Segment Covered](../glossary/segment-covered.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Sales Representative Entity](../entities/sales-representatives.md)
- [View Sales Representatives Domain](../domains/sales-representatives.md)
