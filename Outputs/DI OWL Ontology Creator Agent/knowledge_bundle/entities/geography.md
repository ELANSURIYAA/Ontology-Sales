---
title: Geography
type: entity
description: Geographic attributes used to analyze bookings by sales region, theater, and country
resource: entities
tags: [entity, dimension, geography, region, location, territory]
timestamp: 2026-07-28T00:00:00Z
---

# Geography

## Business Definition

Stores geographic attributes used to analyze bookings by sales region, theater, and country.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_geography

**Source System**: QuoteToBooking

**Entity Type**: Dimension

---

## Attributes

- **Geography Key** (geography_key): Surrogate key that uniquely identifies a geography record in the geography dimension
- **Sales Region** (region): High-level geographic region used for reporting and performance analysis
- **Sales Theater** (theater): Subregional sales area or theater used to organize market coverage and reporting
- **Country** (country): Country associated with the geography record

---

## Primary Keys

- **Geography Key** (geography_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- **[Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)**: One-to-Many relationship linking geographies to booking transactions

### Related Entities

- [Booking Transaction](booking-transaction.md): Fact entity that references this dimension
- [Customer](customer.md): Related through headquarters location
- [Sales Representative](sales-representative.md): Related through territory coverage

---

## Measures

This dimension supports analysis of the following measures:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Concepts

- [Geography](../glossary/geography.md)
- [Geography Key](../glossary/geography-key.md)
- [Sales Region](../glossary/sales-region.md)
- [Sales Theater](../glossary/sales-theater.md)
- [Country](../glossary/country.md)

---

## Business Rules

1. Geography Key is a surrogate key and must be unique
2. Sales Region represents the highest level of geographic hierarchy
3. Sales Theater represents a subregional sales area within a region
4. Country represents the specific country for the geography
5. Every booking transaction must reference a valid geography
6. Geography hierarchy supports drill-down analysis from region to theater to country
7. Geographic attributes enable territory-based performance analysis

---

## Usage Examples

**Analysis by Sales Region**:
- Compare booking revenue across major geographic regions
- Analyze regional market performance
- Measure regional growth trends

**Analysis by Sales Theater**:
- Evaluate theater-level sales performance
- Compare theater performance within regions
- Analyze market penetration by theater

**Analysis by Country**:
- Identify top-performing countries by booking revenue
- Analyze country-specific product adoption
- Compare discount rates across countries

**Geographic Hierarchy Analysis**:
- Drill down from region to theater to country
- Roll up country performance to theater and region levels
- Analyze geographic distribution of bookings

**Territory Performance**:
- Measure sales representative effectiveness by geography
- Analyze partner performance by territory
- Compare customer distribution across geographies

---

## Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Main Index](../index.md)
- [View Relationships](../relationships/index.md)
- [View Measures](../measures/index.md)
- [View Glossary](../glossary/index.md)
