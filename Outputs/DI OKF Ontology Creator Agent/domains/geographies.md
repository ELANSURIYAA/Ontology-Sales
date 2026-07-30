---
title: Geographies Domain
type: domain
description: Geographic sales territory attributes used to analyze bookings by region, theater, and country
resource: domains
tags: [geography, territory, region, location, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Geographies Domain

## Business Definition

The Geographies domain stores geographic sales territory attributes used to analyze bookings by region, theater, and country. This domain enables geographic performance analysis and territory management.

---

## Business Purpose

The Geographies domain enables analysis of:

- Regional sales performance
- Theater-level territory analysis
- Country-specific booking trends
- Geographic market penetration
- Territory coverage and effectiveness
- International vs domestic sales mix

---

## Domain Type

**Dimension Domain** - Descriptive attributes for geographic analysis

---

## Related Entities

- [Geography](../entities/geographies.md)

---

## Related Measures

All booking and revenue measures can be analyzed by geographic attributes:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Total Quantity](../measures/total-quantity.md)

---

## Related Relationships

- [Bookings to Geographies](../relationships/bookings-to-geographies.md)

---

## Key Concepts

### Region
High-level geographic region used for sales reporting, such as Americas, EMEA, or APJC.

### Theater
Intermediate sales territory grouping within a region for operational management.

### Country
Country-level geographic classification for detailed market analysis.

---

## Semantic Links

### Related Domains
- [Bookings Domain](bookings.md) - Geographic sales
- [Customers Domain](customers.md) - Customer location
- [Sales Representatives Domain](sales-representatives.md) - Territory assignment

### Related Glossary
- [Region](../glossary/region.md)
- [Theater](../glossary/theater.md)
- [Country](../glossary/country.md)

---

## Technical Mapping

**Source Table**: quotetobooking.dim_geography  
**Primary Key**: geography_key

---

## Navigation

- [Return to Domains Index](index.md)
- [Return to Main Index](../index.md)
- [View Geography Entity](../entities/geographies.md)
