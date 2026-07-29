---
title: Headquarters Country
type: glossary
description: Country where the customer organization's headquarters is located
resource: glossary
tags: [customer, country, location, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Headquarters Country

## Business Definition

Country where the customer organization's headquarters is located.

---

## Business Meaning

Headquarters Country identifies the primary country location of the customer's corporate headquarters. This attribute supports geographic analysis and enables understanding of customer distribution by headquarters location.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_customer  
**Source Column:** hq_country  
**Data Type:** Character Varying(40)  
**Entity:** [Customer](../entities/customer.md)  
**Attribute:** Headquarters Country  
**Confidence Score:** 1.00

---

## Related Concepts

- [Customer](./customer.md) - Parent entity
- [Headquarters Region](./headquarters-region.md) - Regional location
- [Geography](./geography.md) - Geographic dimension

---

## Usage Context

Headquarters Country is used to:
- Identify customer headquarters location
- Enable geographic customer analysis
- Support regional market strategies
- Track customer distribution by country

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/customer.md)
- [Return to Bundle Index](../index.md)
