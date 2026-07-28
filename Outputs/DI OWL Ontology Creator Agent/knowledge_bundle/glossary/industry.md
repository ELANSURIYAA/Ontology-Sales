---
title: Industry
type: glossary
description: Industry in which the customer operates
resource: glossary
tags: [glossary, customer, industry, vertical, sector]
timestamp: 2026-07-28T00:00:00Z
---

# Industry

## Business Definition

Identifies the industry in which the customer operates.

---

## Business Meaning

Industry classifies customers by their primary business sector or vertical market. Industry classification enables analysis of market penetration, industry-specific performance, and targeted go-to-market strategies. Different industries often have unique technology needs, buying patterns, and regulatory requirements.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_customer  
**Source Column**: industry  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Industry  
**Data Type**: character varying(40)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Vertical
- Industry Vertical
- Business Sector
- Market Vertical

---

## Related Concepts

### Related Entities
- [Customer](../entities/customer.md)

### Related Attributes
- [Customer Segment](customer-segment.md)
- [Customer Key](customer-key.md)

---

## Usage Context

Industry is used to:
- Analyze revenue by industry vertical
- Identify high-performing sectors
- Target industry-specific solutions
- Assess market penetration

---

## Examples

- Financial Services
- Healthcare
- Manufacturing
- Retail
- Telecommunications
- Government

---

## Navigation

- [View Glossary Index](index.md)
- [View Customer Entity](../entities/customer.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Customer  
**Source Attribute**: Industry  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
