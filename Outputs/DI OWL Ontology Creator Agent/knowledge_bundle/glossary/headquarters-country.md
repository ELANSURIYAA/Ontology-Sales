---
title: Headquarters Country
type: glossary
description: Country where the customer organization's headquarters is located
resource: glossary
tags: [glossary, customer, location, country]
timestamp: 2026-07-28T00:00:00Z
---

# Headquarters Country

## Business Definition

Country where the customer organization's headquarters is located.

## Business Meaning

Headquarters Country identifies the primary country location of the customer's corporate headquarters. This geographic attribute enables analysis of customer distribution, regional market penetration, and international vs domestic customer mix.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer  
**Source Column**: hq_country  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Headquarters Country  
**Data Type**: Character Varying(40)  
**Confidence Score**: 1.00

## Synonyms

- HQ Country
- Home Country
- Corporate Country

## Related Concepts

- [Customer](./customer.md)
- [Headquarters Region](./headquarters-region.md)
- [Geography](./geography.md)
- [Country](./country.md)

## Usage Context

Headquarters Country is used to:
- Analyze customer geographic distribution
- Track international market penetration
- Support regional sales planning
- Enable country-specific analysis

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Customer (ENT002)  
**Attribute**: ATTR012
