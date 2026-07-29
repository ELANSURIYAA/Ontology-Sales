---
title: Customer Segment
type: glossary
description: Classifies the customer into a business segment such as Enterprise, Service Provider, or Public Sector
resource: glossary
tags: [customer, segment, classification, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Customer Segment

## Business Definition

Classifies the customer into a business segment such as Enterprise, Service Provider, or Public Sector.

---

## Business Meaning

Customer Segment categorizes customers based on their business model, organizational structure, and market focus. This classification enables targeted analysis, sales strategies, and product positioning for different customer types.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_customer  
**Source Column:** segment  
**Data Type:** Character Varying(30)  
**Entity:** [Customer](../entities/customer.md)  
**Attribute:** Customer Segment  
**Confidence Score:** 1.00

---

## Related Concepts

- [Customer](./customer.md) - Parent entity
- [Industry](./industry.md) - Industry classification
- [Account Tier](./account-tier.md) - Strategic importance
- [Covered Segment](./covered-segment.md) - Sales representative coverage

---

## Usage Context

Customer Segment is used to:
- Categorize customers by business type
- Enable segment-specific analysis and reporting
- Support targeted sales and marketing strategies
- Track segment mix and performance

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/customer.md)
- [Return to Bundle Index](../index.md)
