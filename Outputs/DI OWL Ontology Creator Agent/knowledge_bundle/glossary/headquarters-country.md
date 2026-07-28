---
title: Headquarters Country
type: glossary
description: Country where the customer organization's headquarters is located
resource: glossary
tags: [glossary, customer, country, location, headquarters]
timestamp: 2026-07-28T00:00:00Z
---

# Headquarters Country

## Business Definition

Country where the customer organization's headquarters is located.

---

## Business Meaning

Headquarters Country identifies the primary country location of the customer's corporate headquarters. This geographic attribute enables analysis of customer distribution, regional market penetration, and headquarters-based segmentation. It differs from transaction geography, which represents where sales occur.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_customer  
**Source Column**: hq_country  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Headquarters Country  
**Data Type**: character varying(40)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- HQ Country
- Home Country
- Corporate Country
- Headquarters Location

---

## Related Concepts

### Related Entities
- [Customer](../entities/customer.md)
- [Geography](../entities/geography.md)

### Related Attributes
- [Headquarters Region](headquarters-region.md)
- [Customer Key](customer-key.md)

---

## Usage Context

Headquarters Country is used to:
- Analyze customer distribution by country
- Assess market penetration
- Support regional sales planning
- Identify geographic customer concentrations

---

## Navigation

- [View Glossary Index](index.md)
- [View Customer Entity](../entities/customer.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Customer  
**Source Attribute**: Headquarters Country  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
