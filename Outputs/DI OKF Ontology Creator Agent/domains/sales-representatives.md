---
title: Sales Representatives Domain
type: domain
description: Sales persons responsible for managing customer relationships and booking transactions, including role, team, and segment coverage
resource: domains
tags: [sales-rep, sales-team, seller, performance, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Sales Representatives Domain

## Business Definition

The Sales Representatives domain stores information about the sales person responsible for managing customer relationships and booking transactions, including role, team, and segment coverage. This domain enables sales performance analysis and quota management.

---

## Business Purpose

The Sales Representatives domain enables analysis of:

- Individual sales representative performance
- Sales team effectiveness
- Role-based performance comparison
- Segment coverage analysis
- Quota attainment tracking
- Sales capacity planning

---

## Domain Type

**Dimension Domain** - Descriptive attributes for sales representative analysis

---

## Related Entities

- [Sales Representative](../entities/sales-representatives.md)

---

## Related Measures

All booking and revenue measures can be analyzed by sales representative attributes:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

---

## Related Relationships

- [Bookings to Sales Representatives](../relationships/bookings-to-sales-representatives.md)

---

## Key Concepts

### Sales Role
Job role or selling responsibility of the sales representative such as Account Executive or Sales Engineer.

### Sales Team
Team or organizational unit the sales representative belongs to for management structure.

### Segment Covered
Customer segment or market segment covered by the sales representative for territory alignment.

---

## Semantic Links

### Related Domains
- [Bookings Domain](bookings.md) - Sales representative bookings
- [Customers Domain](customers.md) - Account ownership
- [Geographies Domain](geographies.md) - Territory coverage

### Related Glossary
- [Sales Role](../glossary/sales-role.md)
- [Sales Team](../glossary/sales-team.md)
- [Segment Covered](../glossary/segment-covered.md)

---

## Technical Mapping

**Source Table**: quotetobooking.dim_sales_rep  
**Primary Key**: sales_rep_key  
**Business Key**: rep_id

---

## Navigation

- [Return to Domains Index](index.md)
- [Return to Main Index](../index.md)
- [View Sales Representative Entity](../entities/sales-representatives.md)
