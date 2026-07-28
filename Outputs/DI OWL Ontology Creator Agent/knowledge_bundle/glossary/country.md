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

Country represents the most granular level of the geographic hierarchy, identifying the specific nation where sales transactions occur. Country-level analysis enables detailed market assessment, country-specific strategy development, and precise geographic performance measurement.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_geography

**Source Column**: country

**Entity**: [Geography](../entities/geography.md)

**Attribute**: Country

**Data Type**: Character Varying(40)

**Confidence Score**: 1.00

---

## Related Concepts

- [Geography](geography.md)
- [Geography Key](geography-key.md)
- [Sales Region](sales-region.md)
- [Sales Theater](sales-theater.md)
- [Headquarters Country](headquarters-country.md)

---

## Usage Context

Country is used to:
- Enable country-level performance analysis
- Support country-specific market strategy
- Facilitate country-based resource allocation
- Enable detailed geographic drill-down
- Support country-level compliance and reporting

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Geography](../entities/geography.md)
- [Back to Main Index](../index.md)
