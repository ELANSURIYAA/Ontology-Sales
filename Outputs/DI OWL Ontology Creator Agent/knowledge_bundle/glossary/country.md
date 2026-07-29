---
title: Country
type: glossary
description: Country associated with the geography record
resource: glossary
tags: [geography, country, location, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Country

## Business Definition

Country associated with the geography record.

---

## Business Meaning

Country represents the specific nation where booking transactions occur, providing the most granular level of geographic analysis. This enables country-specific performance tracking and market analysis.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_geography  
**Source Column:** country  
**Data Type:** Character Varying(40)  
**Entity:** [Geography](../entities/geography.md)  
**Attribute:** Country  
**Confidence Score:** 1.00

---

## Related Concepts

- [Geography](./geography.md) - Parent entity
- [Sales Region](./sales-region.md) - Regional grouping
- [Sales Theater](./sales-theater.md) - Theater grouping

---

## Usage Context

Country is used to:
- Identify specific country locations
- Enable country-level performance analysis
- Support country-specific strategies
- Track market penetration by country

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/geography.md)
- [Return to Bundle Index](../index.md)
