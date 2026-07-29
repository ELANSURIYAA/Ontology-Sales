---
title: Headquarters Region
type: glossary
description: Global region where the customer organization's headquarters is located
resource: glossary
tags: [customer, region, location, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Headquarters Region

## Business Definition

Global region where the customer organization's headquarters is located.

---

## Business Meaning

Headquarters Region identifies the global geographic region of the customer's corporate headquarters. This attribute enables high-level regional analysis and strategic planning by customer location.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_customer  
**Source Column:** hq_region  
**Data Type:** Character Varying(20)  
**Entity:** [Customer](../entities/customer.md)  
**Attribute:** Headquarters Region  
**Confidence Score:** 1.00

---

## Related Concepts

- [Customer](./customer.md) - Parent entity
- [Headquarters Country](./headquarters-country.md) - Country location
- [Geography](./geography.md) - Geographic dimension

---

## Usage Context

Headquarters Region is used to:
- Identify customer headquarters region
- Enable regional customer analysis
- Support global market strategies
- Track customer distribution by region

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/customer.md)
- [Return to Bundle Index](../index.md)
