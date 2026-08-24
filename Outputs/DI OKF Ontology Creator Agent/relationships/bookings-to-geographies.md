---
title: Bookings to Geographies
type: relationship
description: Links booking transactions to geographic territories
resource: relationships
tags: [bookings, geographies, many-to-one, relationship, territory]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Geographies

## Business Definition

The Bookings to Geographies relationship links individual booking transactions to geographic sales territories. This relationship enables analysis of booking performance by region, theater, and country, supporting territory-based sales planning, geographic expansion strategies, and regional performance tracking.

---

## Relationship Type

**Many-to-one**

Multiple booking transactions can be associated with the same geographic territory.

---

## Source Entity

**[Bookings](../entities/bookings.md)**

The fact table containing individual completed sales booking transactions.

---

## Target Entity

**[Geographies](../entities/geographies.md)**

The dimension table containing geographic sales territory attributes.

---

## Cardinality

**Many Bookings : One Geography**

- Each booking transaction references exactly one geography record
- Multiple booking transactions can be associated with the same geography
- Geography records can exist without associated bookings

---

## Join Specification

### Left Join Key
- **Field**: geography_key
- **Entity**: Bookings
- **Type**: Foreign Key

### Right Join Key
- **Field**: geography_key
- **Entity**: Geographies
- **Type**: Primary Key

### Join Condition
```sql
bookings.geography_key = geographies.geography_key
```

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings

**Target Table**: quotetobooking.dim_geography

**Join Column**: geography_key

---

## Business Purpose

This relationship enables:

- **Regional Analysis**: Analyze booking performance by region (Americas, EMEA, APJC)
- **Theater Analysis**: Track booking patterns by sales theater
- **Country Analysis**: Evaluate performance by country
- **Territory Planning**: Support territory-based sales planning and quota allocation
- **Geographic Expansion**: Identify opportunities for geographic expansion
- **Regional Comparisons**: Compare performance across regions and theaters

---

## Related Measures

All booking measures can be analyzed by geographic attributes:
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

1. **Mandatory Relationship**: Every booking must reference a valid geography
2. **Referential Integrity**: geography_key in bookings must exist in geographies dimension
3. **One Geography per Booking**: Each booking references exactly one geography record
4. **Geography Independence**: Geographies can exist without bookings (defined territories)

---

## Usage Examples

### Regional Analysis
```sql
SELECT 
    geographies.region,
    COUNT(bookings.booking_id) as booking_count,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN geographies ON bookings.geography_key = geographies.geography_key
GROUP BY geographies.region
```

### Country Analysis
```sql
SELECT 
    geographies.country,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN geographies ON bookings.geography_key = geographies.geography_key
GROUP BY geographies.country
ORDER BY total_booking_amount DESC
```

---

## Data Quality Rules

- geography_key in bookings must not be null
- geography_key in bookings must reference valid geography_key in geographies
- No orphaned bookings without geography references
- Geography dimension must be populated before booking transactions

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
