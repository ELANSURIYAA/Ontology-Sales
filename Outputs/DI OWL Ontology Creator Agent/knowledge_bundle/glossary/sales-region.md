---
title: Sales Region
type: glossary
description: High-level geographic region used for reporting and performance analysis
resource: glossary
tags: [glossary, geography, region, sales-territory]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Region

## Business Definition

High-level geographic region used for reporting and performance analysis.

---

## Business Meaning

Sales Region represents the highest level of geographic organization for sales operations. It enables executive-level regional performance analysis and strategic market planning across major geographic markets.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_geography  
**Source Column**: region  
**Entity**: [Geography](../entities/geography.md)  
**Attribute**: Sales Region  
**Data Type**: character varying(20)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Region
- Geographic Region
- Market Region

---

## Related Concepts

### Related Entities
- [Geography](../entities/geography.md)

### Related Attributes
- [Geography Key](geography-key.md)
- [Sales Theater](sales-theater.md)
- [Country](country.md)

---

## Usage Context

Sales Region is used to:
- Support executive-level regional reporting
- Compare performance across major markets
- Guide regional strategy and resource allocation

---

## Examples

- Americas
- EMEA
- APAC

---

## Navigation

- [View Glossary Index](index.md)
- [View Geography Entity](../entities/geography.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Geography  
**Source Attribute**: Sales Region  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
