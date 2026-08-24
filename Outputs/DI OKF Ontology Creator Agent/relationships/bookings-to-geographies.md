---
title: Bookings to Geographies
type: relationship
description: Links booking transactions to geographic sales territories
resource: relationships
tags: [bookings, geographies, relationship, many-to-one]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Geographies

## Business Definition

Links booking transactions to geographic sales territory attributes used to analyze bookings by region, theater, and country.

This relationship enables geographic analysis of booking performance and supports market penetration and regional sales effectiveness analysis.

---

## Relationship Type

**many-to-one**

Multiple booking transactions can be associated with the same geography.

---

## Source Entity

[Bookings](../entities/bookings.md)

---

## Target Entity

[Geographies](../entities/geographies.md)

---

## Cardinality

- Each booking transaction must be associated with exactly one geography record
- Each geography record can be associated with multiple booking transactions

---

## Technical Mapping

**Join Condition**: bookings.geography_key = geographies.geography_key

**Left Dataset**: bookings (quotetobooking.fact_bookings)

**Right Dataset**: geographies (quotetobooking.dim_geography)

**Join Keys**:
- Left: geography_key
- Right: geography_key

---

## Business Purpose

This relationship enables:
- Regional performance analysis (Americas, EMEA, APJC)
- Theater-level sales territory analysis
- Country-specific market analysis
- Geographic market penetration tracking
- Regional quota and target management
- Cross-regional performance comparisons

---

## Related Measures

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Booking Count](../measures/booking-count.md)

---

## Related Concepts

- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
