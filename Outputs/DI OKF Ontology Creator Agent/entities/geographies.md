---
title: Geographies
type: entity
description: Geographic sales territories with region, theater, and country attributes
resource: entities
tags: [geographies, dimension, territories]
timestamp: 2026-07-28T00:00:00Z
---

# Geographies

## Business Definition

Stores geographic sales territory attributes used to analyze bookings by region, theater, and country.

Geographies represent the sales territories and geographic markets where booking transactions occur.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_geography

**Source Columns**: geography_key, region, theater, country

---

## Attributes

- **geography_key** - Surrogate key that uniquely identifies a geography record in the geography dimension
- **region** - High-level geographic region used for sales reporting, such as Americas, EMEA, or APJC
- **theater** - Intermediate sales territory grouping within a region
- **country** - Country associated with the geography record

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

All booking-related measures can be analyzed by geographic attributes:
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Booking Count](../measures/booking-count.md)

---

## Related Concepts

- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

- Each geography must have a unique geography_key
- Geographies are organized hierarchically: country → theater → region
- Region represents the highest level of geographic aggregation
- Theater provides intermediate grouping within regions
- Country provides the most granular geographic detail
- Geographic analysis enables market penetration and regional performance tracking

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
