---
title: Customer Segment
type: glossary
description: Classification of customers into business segments such as Enterprise, Service Provider, or Public Sector
resource: glossary
tags: [glossary, customer, segment, classification]
timestamp: 2026-07-28T00:00:00Z
---

# Customer Segment

## Business Definition

Classifies the customer into a business segment such as Enterprise, Service Provider, or Public Sector.

---

## Business Meaning

Customer Segment categorizes customers based on their business model, size, and operational characteristics. Segmentation enables targeted sales strategies, customized product offerings, and segment-specific performance analysis. Different segments often have distinct buying behaviors, needs, and value propositions.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_customer  
**Source Column**: segment  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Customer Segment  
**Data Type**: character varying(30)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Market Segment
- Customer Category
- Business Segment
- Customer Type

---

## Related Concepts

### Related Entities
- [Customer](../entities/customer.md)

### Related Attributes
- [Customer Key](customer-key.md)
- [Industry](industry.md)
- [Account Tier](account-tier.md)

---

## Usage Context

Customer Segment is used to:
- Analyze revenue by customer type
- Target sales and marketing efforts
- Customize product offerings
- Assess segment-specific performance

---

## Examples

- Enterprise
- Service Provider
- Public Sector
- Mid-Market
- Small Business

---

## Navigation

- [View Glossary Index](index.md)
- [View Customer Entity](../entities/customer.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Customer  
**Source Attribute**: Customer Segment  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
