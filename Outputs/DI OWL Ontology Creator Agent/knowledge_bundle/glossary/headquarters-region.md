---
title: Headquarters Region
type: glossary
description: Global region where the customer organization's headquarters is located
resource: glossary
tags: [glossary, customer, location, region]
timestamp: 2026-07-28T00:00:00Z
---

# Headquarters Region

## Business Definition

Global region where the customer organization's headquarters is located.

## Business Meaning

Headquarters Region identifies the high-level geographic region of the customer's corporate headquarters. This enables regional analysis of customer base, supports global market segmentation, and facilitates regional sales strategy development.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer  
**Source Column**: hq_region  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Headquarters Region  
**Data Type**: Character Varying(20)  
**Confidence Score**: 1.00

## Synonyms

- HQ Region
- Home Region
- Corporate Region

## Related Concepts

- [Customer](./customer.md)
- [Headquarters Country](./headquarters-country.md)
- [Geography](./geography.md)
- [Sales Region](./sales-region.md)

## Usage Context

Headquarters Region is used to:
- Analyze customer regional distribution
- Support global market analysis
- Enable regional customer segmentation
- Track regional market penetration

## Example Values

- Americas
- EMEA
- APAC
- North America
- Europe

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Customer (ENT002)  
**Attribute**: ATTR013
