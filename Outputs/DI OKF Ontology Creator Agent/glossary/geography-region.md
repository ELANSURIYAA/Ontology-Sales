---
title: Geography Region
type: glossary
description: High-level geographic region used for sales reporting and territory management
resource: glossary
tags: [geography, region, territory]
timestamp: 2026-07-28T00:00:00Z
---

# Geography Region

## Business Definition

Geography Region is a high-level geographic region used for sales reporting and territory management. Regions represent broad geographic areas that organize sales territories and enable regional performance analysis.

---

## Business Meaning

Geography Region is used to:
- Organize sales territories at a high level
- Support regional sales management and reporting
- Enable geographic performance analysis
- Guide regional resource allocation
- Support regional go-to-market strategies
- Enable regional competitive analysis

Common geographic regions include:
- **Americas**: North America, Latin America, South America
- **EMEA**: Europe, Middle East, Africa
- **APJC**: Asia Pacific, Japan, China
- **North America**: United States, Canada
- **Europe**: European countries
- **Asia Pacific**: Asian and Pacific countries

---

## Technical Mapping

**Source Entity**: [Geographies](../entities/geographies.md)

**Source Field**: region

---

## Synonyms

- Sales Region
- Geographic Region
- Territory Region
- Regional Territory
- Geo Region

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Transactions analyzed by geography region

---

## Related Entities

- [Geographies](../entities/geographies.md) - Contains region classification
- [Customers](../entities/customers.md) - Customer headquarters region

---

## Related Measures

All booking measures can be analyzed by geography region:
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Total ACV USD](../measures/total-acv-usd.md)

---

## Usage Context

Geography Region is used for:
- Regional sales reporting
- Territory planning and management
- Regional performance tracking
- Resource allocation by region
- Regional quota setting
- Market expansion planning
- Regional competitive analysis

---

## Business Rules

1. Each geography record is assigned to a region
2. Regions represent the highest level of geographic hierarchy
3. Region classification is standardized across the organization
4. Regions may contain multiple theaters and countries

---

## Geographic Hierarchy

**Region** (highest level)
- Theater (mid-level)
  - Country (lowest level)

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
