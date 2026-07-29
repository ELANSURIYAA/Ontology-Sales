---
title: Geography Domain
type: domain
description: Geographic master data used to analyze bookings by region, theater, and country
resource: domains
tags: [okf, domain, geography, region, location]
timestamp: 2026-07-28T00:00:00Z
---

# Geography Domain

## Business Definition

The Geography domain encompasses geographic master data used to analyze bookings by region, theater, and country. This domain provides the geographic dimensional context necessary for regional sales analytics and territory management.

---

## Business Purpose

This domain enables business users to:

- Analyze sales performance by geographic region
- Track revenue by theater and country
- Monitor regional growth trends
- Support territory planning and coverage
- Evaluate geographic market penetration
- Compare performance across geographies
- Enable location-based sales strategies

---

## Domain Scope

### Included
- Global sales regions
- Sales theaters (sub-regions)
- Country classifications
- Geographic hierarchies (Region → Theater → Country)

### Excluded
- Customer headquarters location (covered in Customer Management domain)
- Detailed address information
- Postal codes and zip codes
- City and state/province details
- Geographic coordinates

---

## Related Entities

### Primary Entities
- [Geography Dimension](../entities/geography-dimension.md)

---

## Related Measures

All sales and revenue measures can be analyzed by geographic attributes:

- [Quantity Sold](../measures/quantity-sold.md) by geography
- [Booking Amount USD](../measures/booking-amount-usd.md) by geography
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md) by geography
- [Total Contract Value USD](../measures/total-contract-value-usd.md) by geography
- [Unit List Price USD](../measures/unit-list-price-usd.md) by geography
- [Discount Percentage](../measures/discount-percentage.md) by geography

---

## Related Relationships

- [Geography to Booking](../relationships/geography-to-booking.md)

---

## Key Business Concepts

### Region
Broad global sales region such as:
- **Americas**: North America, Latin America, and Caribbean
- **EMEA**: Europe, Middle East, and Africa
- **APJC**: Asia Pacific, Japan, and China

### Theater
Sales theater or sub-region used for operational reporting within a region. Theaters provide more granular geographic segmentation for sales management and territory assignment.

### Country
Individual country associated with the booking transaction, enabling country-level analysis and compliance reporting.

### Geographic Hierarchy
The geography dimension supports hierarchical analysis:
- **Level 1**: Region (highest level)
- **Level 2**: Theater (mid level)
- **Level 3**: Country (lowest level)

---

## Business Rules

1. Every geography record must have a unique Geography Key (surrogate key)
2. Region should be populated for all geography records
3. Theater should align with parent Region
4. Country should align with parent Theater and Region
5. Country names should follow standard country code conventions
6. Geographic hierarchies must be logically consistent

---

## Analytical Use Cases

### Regional Performance Analysis
- Compare revenue and bookings across global regions
- Track regional growth rates and trends
- Identify regional market opportunities
- Monitor regional quota attainment

### Theater Analysis
- Analyze performance by sales theater
- Compare theaters within regions
- Support theater-level planning and resource allocation
- Track theater-specific initiatives and campaigns

### Country Analysis
- Track revenue by country
- Identify top performing countries
- Analyze country-specific trends and seasonality
- Support country-level compliance and reporting

### Geographic Segmentation
- Segment customers by geography
- Analyze product adoption by geography
- Identify geographic expansion opportunities
- Support territory planning and coverage optimization

### Cross-Geographic Analysis
- Compare performance across regions, theaters, and countries
- Identify geographic best practices
- Analyze geographic market share
- Support global sales strategy

---

## Data Quality Metrics

### Completeness
- Geography Key must be populated for all records
- Region should be populated (>95% target)
- Theater should be populated (>90% target)
- Country should be populated (>90% target)

### Accuracy
- Geography Key must be unique
- Region must match approved region values
- Theater must match approved theater values
- Country must match standard country codes
- Geographic hierarchies must be valid

### Consistency
- Theater must align with parent Region
- Country must align with parent Theater
- Geographic attributes must be consistent across all bookings
- Geography master data must reconcile with source systems

---

## Technical Implementation

### Source System
- **Schema**: quotetobooking
- **Table**: dim_geography
- **Primary Key**: geography_key (surrogate key)
- **Type**: Slowly Changing Dimension (Type 1 or Type 2)

### Key Attributes
- Geography Key (Primary Key)
- Region
- Theater
- Country

### Hierarchy Structure
```
Region
└── Theater
    └── Country
```

---

## Semantic Links

### Related Domains
- [Sales Transactions](sales-transactions.md)
- [Customer Management](customer-management.md)
- [Sales Organization](sales-organization.md)
- [Partner Management](partner-management.md)

### Related Glossary Terms
- [Geography Dimension](../glossary/geography-dimension.md)
- [Geography Key](../glossary/geography-key.md)
- [Region](../glossary/region.md)
- [Theater](../glossary/theater.md)
- [Country](../glossary/country.md)

---

## Navigation

- [Back to Domains Index](index.md)
- [Back to Bundle Index](../index.md)
