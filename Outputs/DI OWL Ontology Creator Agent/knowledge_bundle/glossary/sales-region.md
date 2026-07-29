---
title: Sales Region
type: glossary
description: High-level geographic region used for reporting and performance analysis
resource: glossary
tags: [geography, region, sales, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Region

## Business Definition

High-level geographic region used for reporting and performance analysis.

---

## Business Meaning

Sales Region represents the highest level of geographic hierarchy, grouping territories into major geographic areas for strategic planning and performance tracking. Regions enable executive-level geographic analysis.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_geography  
**Source Column:** region  
**Data Type:** Character Varying(20)  
**Entity:** [Geography](../entities/geography.md)  
**Attribute:** Sales Region  
**Confidence Score:** 1.00

---

## Related Concepts

- [Geography](./geography.md) - Parent entity
- [Sales Theater](./sales-theater.md) - Subregional area
- [Country](./country.md) - Country location

---

## Usage Context

Sales Region is used to:
- Group territories into major geographic areas
- Enable high-level regional performance analysis
- Support strategic planning and resource allocation
- Track regional market trends

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/geography.md)
- [Return to Bundle Index](../index.md)
