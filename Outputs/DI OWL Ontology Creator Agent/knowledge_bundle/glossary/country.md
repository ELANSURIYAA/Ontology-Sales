---
title: Country
type: glossary
description: Country associated with the geography record
resource: glossary
tags: [glossary, geography, country, location]
timestamp: 2026-07-28T00:00:00Z
---

# Country

## Business Definition

Country associated with the geography record.

## Business Meaning

Country represents the most granular level of the geographic hierarchy, enabling country-specific analysis, market penetration tracking, and local market performance evaluation.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_geography  
**Source Column**: country  
**Entity**: [Geography](../entities/geography.md)  
**Attribute**: Country  
**Data Type**: Character Varying(40)  
**Confidence Score**: 1.00

## Synonyms

- Nation
- Country Name

## Related Concepts

- [Geography](./geography.md)
- [Sales Region](./sales-region.md)
- [Sales Theater](./sales-theater.md)
- [Headquarters Country](./headquarters-country.md)

## Usage Context

Country is used to:
- Enable country-specific analysis
- Track local market performance
- Support country-level reporting
- Analyze market penetration by country

## Example Values

- United States
- United Kingdom
- Germany
- Japan
- Australia

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Geography (ENT004)  
**Attribute**: ATTR024
