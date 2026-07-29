---
title: Sales Representative ID
type: glossary
description: Business identifier assigned to the sales representative
resource: glossary
tags: [sales, representative, identifier, business-key, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative ID

## Business Definition

Business identifier assigned to the sales representative.

---

## Business Meaning

Sales Representative ID is the business-recognized identifier used to reference sales personnel in operational systems and business communications. Unlike the surrogate Sales Representative Key, this is a meaningful business identifier.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_sales_rep  
**Source Column:** rep_id  
**Data Type:** Character Varying(20)  
**Entity:** [Sales Representative](../entities/sales-representative.md)  
**Attribute:** Sales Representative ID  
**Confidence Score:** 1.00

---

## Related Concepts

- [Sales Representative](./sales-representative.md) - Parent entity
- [Sales Representative Key](./sales-representative-key.md) - Surrogate identifier
- [Sales Representative Name](./sales-representative-name.md) - Person name

---

## Usage Context

Sales Representative ID is used to:
- Reference sales personnel in business processes
- Integrate with operational systems
- Support sales representative lookup and identification
- Enable cross-system personnel tracking

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/sales-representative.md)
- [Return to Bundle Index](../index.md)
