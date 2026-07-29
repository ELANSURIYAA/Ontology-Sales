---
title: Geography Dimension
type: entity
description: Geographic attributes used to analyze bookings by region, theater, and country
resource: entities
tags: [okf, entity, geography, dimension, location]
timestamp: 2026-07-28T00:00:00Z
---

# Geography Dimension

## Business Definition

The Geography Dimension stores geographic attributes used to analyze bookings by region, theater, and country. This dimension enables regional sales analytics and supports territory management and geographic performance analysis.

---

## Technical Mapping

**Source Schema**: quotetobooking  
**Source Table**: dim_geography  
**Entity Type**: Dimension  
**Grain**: One record per unique geographic combination

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

None (this is a dimension table)

---

## Relationships

### Outbound Relationships
- [Geography to Booking](../relationships/geography-to-booking.md) - One-to-Many relationship to Booking Fact

---

## Measures

All booking measures can be analyzed by geographic attributes:

- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Related Concepts

### Related Entities
- [Booking Fact](booking-fact.md)
- [Customer Dimension](customer-dimension.md)

### Related Domains
- [Geography](../domains/geography.md)
- [Sales Transactions](../domains/sales-transactions.md)

### Related Glossary Terms
- [Geography Dimension](../glossary/geography-dimension.md)
- [Geography Key](../glossary/geography-key.md)
- [Region](../glossary/region.md)
- [Theater](../glossary/theater.md)
- [Country](../glossary/country.md)

---

## Business Rules

1. Geography Key must be unique and not null
2. Region should be populated for all geography records
3. Theater should align with parent Region
4. Country should align with parent Theater and Region
5. Country names should follow standard country code conventions
6. Geographic hierarchies must be logically consistent

---

## Attribute Details

### geography_key
- **Data Type**: integer
- **Nullable**: No
- **Primary Key**: Yes
- **Description**: Surrogate key that uniquely identifies a geography record in the geography dimension

### region
- **Data Type**: character varying(20)
- **Nullable**: Yes
- **Description**: Broad global sales region associated with the booking, such as Americas, EMEA, or APJC

### theater
- **Data Type**: character varying(30)
- **Nullable**: Yes
- **Description**: Sales theater or sub-region used for operational reporting within a region

### country
- **Data Type**: character varying(40)
- **Nullable**: Yes
- **Description**: Country associated with the geography record

---

## Analytical Use Cases

- Analyze sales performance by geographic region
- Track revenue by theater and country
- Monitor regional growth trends
- Support territory planning and coverage
- Evaluate geographic market penetration
- Compare performance across geographies

---

## Data Quality Metrics

- **Completeness**: Geography Key must be 100% populated
- **Uniqueness**: Geography Key must be unique
- **Validity**: Region, Theater, and Country must match approved values
- **Consistency**: Theater must align with Region, Country must align with Theater

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Bundle Index](../index.md)
