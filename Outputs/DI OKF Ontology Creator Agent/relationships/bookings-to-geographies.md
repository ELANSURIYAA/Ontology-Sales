---
title: Bookings to Geographies
type: relationship
description: Links booking transactions to the geographic territory where the sale occurred
resource: relationships
tags: [bookings, geographies, relationship, many-to-one]
timestamp: 2024-01-15T00:00:00Z
---

# Bookings to Geographies

## Business Definition

This relationship links booking transactions to the geographic territory where the sale occurred, enabling analysis of bookings by region, theater, and country.

---

## Relationship Details

**Source Entity**: [Booking Transaction](../entities/bookings.md)  
**Target Entity**: [Geography](../entities/geographies.md)  
**Relationship Type**: Many-to-One  
**Cardinality**: Many bookings can be associated with one geography

---

## Technical Mapping

**Join Type**: Inner Join  
**Left Key**: bookings.geography_key  
**Right Key**: geographies.geography_key

---

## Business Description

Each booking transaction is associated with a specific geographic territory that represents where the sale occurred. Geography attributes include region (Americas, EMEA, APJC), theater (intermediate territory grouping), and country. Multiple booking transactions can be associated with the same geography.

---

## Usage

This relationship enables analysis such as:

- Regional sales performance
- Theater-level territory analysis
- Country-specific booking trends
- Geographic market penetration
- International vs domestic sales mix

---

## Related Concepts

- [Region](../glossary/region.md)
- [Theater](../glossary/theater.md)
- [Country](../glossary/country.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
- [View Geography Entity](../entities/geographies.md)
- [View Geographies Domain](../domains/geographies.md)
