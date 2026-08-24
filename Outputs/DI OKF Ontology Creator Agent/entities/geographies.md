---
title: Geographies
type: entity
description: Stores geographic sales territory attributes used to analyze bookings by region, theater, and country
resource: entities
tags: [geographies, dimension, region, territory]
timestamp: 2026-07-28T00:00:00Z
---

# Geographies

## Business Definition

The Geographies entity represents the dimension table that stores geographic sales territory attributes. Each record contains hierarchical geographic classifications including region, theater, and country. This entity enables analysis of booking transactions by geographic location and supports territory-based sales planning and performance tracking.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_geography

**Source Schema**: quotetobooking

**Entity Type**: Dimension Table

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

All booking-related measures can be analyzed by geographic attributes:
- [Booking Count](../measures/booking-count.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Total Quantity](../measures/total-quantity.md)

---

## Related Concepts

- [Geography Region](../glossary/geography-region.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

1. **Unique Geography Key**: Each geography record must have a unique geography_key
2. **Geographic Hierarchy**: Geography is organized hierarchically as Region → Theater → Country
3. **Region Classification**: High-level geographic regions such as Americas, EMEA, or APJC
4. **Theater Grouping**: Intermediate sales territory groupings within regions
5. **Country Level**: Specific country associated with the geography record

---

## Attribute Definitions

### geography_key
Surrogate key that uniquely identifies a geography record in the geography dimension. Used as the primary key and referenced by the bookings fact table.

### region
High-level geographic region used for sales reporting, such as Americas, EMEA, or APJC. Provides the top level of the geographic hierarchy.

### theater
Intermediate sales territory grouping within a region. Provides mid-level geographic aggregation for sales management and reporting.

### country
Country associated with the geography record. Provides the most granular level of geographic analysis.

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Usage Examples

### Regional Analysis
- Analyze booking amount by region
- Compare Americas vs EMEA vs APJC performance
- Track regional growth trends

### Theater Analysis
- Evaluate theater performance within regions
- Identify top-performing theaters
- Support theater-level sales planning

### Country Analysis
- Analyze booking distribution by country
- Identify country-specific opportunities
- Support country-level market analysis

### Geographic Hierarchy Analysis
- Roll up country performance to theater level
- Aggregate theater performance to region level
- Support multi-level geographic reporting

---

## Data Quality Checks

- geography_key is unique and not null
- region is not null and is a valid region code
- theater is not null and is a valid theater designation
- country is not null and is a valid country code
- Geographic hierarchy is consistent (country → theater → region)
