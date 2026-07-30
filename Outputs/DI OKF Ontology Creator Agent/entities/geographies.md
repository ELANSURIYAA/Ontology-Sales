---
title: Geography
type: entity
description: Geographic sales territory attributes used to analyze bookings by region, theater, and country
resource: entities
tags: [geography, territory, region, location, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Geography

## Business Definition

The Geography entity stores geographic sales territory attributes used to analyze bookings by region, theater, and country. This entity enables geographic performance analysis and territory management.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_geography  
**Source Schema**: quotetobooking  
**Entity Type**: Dimension  
**Grain**: One row per geography

---

## Attributes

- geography_key
- region
- theater
- country

---

## Primary Keys

- geography_key

---

## Foreign Keys

None

---

## Relationships

- [Bookings to Geographies](../relationships/bookings-to-geographies.md)

---

## Measures

All booking and revenue measures can be analyzed by geographic attributes:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Total Quantity](../measures/total-quantity.md)

---

## Related Concepts

- [Region](../glossary/region.md)
- [Theater](../glossary/theater.md)
- [Country](../glossary/country.md)

---

## Business Rules

### Geographic Hierarchy
Geography follows a three-level hierarchy: Region → Theater → Country.

### Region Classification
Regions represent high-level geographic areas such as Americas, EMEA, or APJC.

### Theater Grouping
Theaters represent intermediate sales territory groupings within a region for operational management.

### Country Assignment
Country represents the specific country associated with the geography record for detailed market analysis.

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Geographies Domain](../domains/geographies.md)
