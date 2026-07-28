---
title: Headquarters Region
type: glossary
description: Global region where the customer organization's headquarters is located
resource: glossary
tags: [glossary, customer, region, location, headquarters]
timestamp: 2026-07-28T00:00:00Z
---

# Headquarters Region

## Business Definition

Global region where the customer organization's headquarters is located.

---

## Business Meaning

Headquarters Region identifies the high-level geographic region where the customer's corporate headquarters is based. This regional classification enables analysis of customer distribution across major global markets and supports regional sales and marketing strategies.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_customer  
**Source Column**: hq_region  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Headquarters Region  
**Data Type**: character varying(20)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- HQ Region
- Home Region
- Corporate Region
- Headquarters Geographic Region

---

## Related Concepts

### Related Entities
- [Customer](../entities/customer.md)
- [Geography](../entities/geography.md)

### Related Attributes
- [Headquarters Country](headquarters-country.md)
- [Customer Key](customer-key.md)

---

## Usage Context

Headquarters Region is used to:
- Analyze customer distribution by global region
- Support regional market analysis
- Enable geographic customer segmentation
- Guide regional sales strategies

---

## Examples

- Americas
- EMEA (Europe, Middle East, Africa)
- APAC (Asia Pacific)
- Latin America

---

## Navigation

- [View Glossary Index](index.md)
- [View Customer Entity](../entities/customer.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Customer  
**Source Attribute**: Headquarters Region  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
