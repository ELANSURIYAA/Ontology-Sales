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

---

## Business Meaning

Country represents the specific nation where sales transactions occur. It provides the most granular level of geographic analysis and enables country-specific market analysis, regulatory compliance, and localization strategies.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_geography  
**Source Column**: country  
**Entity**: [Geography](../entities/geography.md)  
**Attribute**: Country  
**Data Type**: character varying(40)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Nation
- Country Name

---

## Related Concepts

### Related Entities
- [Geography](../entities/geography.md)

### Related Attributes
- [Sales Region](sales-region.md)
- [Sales Theater](sales-theater.md)
- [Geography Key](geography-key.md)

---

## Usage Context

Country is used to:
- Support country-level sales analysis
- Enable market-specific strategies
- Track country performance

---

## Navigation

- [View Glossary Index](index.md)
- [View Geography Entity](../entities/geography.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Geography  
**Source Attribute**: Country  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
