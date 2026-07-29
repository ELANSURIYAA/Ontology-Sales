---
title: Sales Region
type: glossary
description: High-level geographic region used for reporting and performance analysis
resource: glossary
tags: [glossary, geography, region, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Region

## Business Definition

High-level geographic region used for reporting and performance analysis.

## Business Meaning

Sales Region represents the highest level of geographic hierarchy, typically covering major global areas. It enables executive-level regional performance analysis and strategic market planning.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_geography  
**Source Column**: region  
**Entity**: [Geography](../entities/geography.md)  
**Attribute**: Sales Region  
**Data Type**: Character Varying(20)  
**Confidence Score**: 1.00

## Synonyms

- Region
- Geographic Region
- Market Region

## Related Concepts

- [Geography](./geography.md)
- [Sales Theater](./sales-theater.md)
- [Country](./country.md)

## Usage Context

Sales Region is used to:
- Enable high-level regional reporting
- Support strategic market analysis
- Track regional performance
- Allocate regional resources

## Example Values

- Americas
- EMEA
- APAC
- North America
- Europe

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Geography (ENT004)  
**Attribute**: ATTR022
