---
title: Sales Representative Name
type: glossary
description: Full name of the sales representative associated with the booking
resource: glossary
tags: [sales, representative, name, person, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative Name

## Business Definition

Full name of the sales representative associated with the booking.

---

## Business Meaning

Sales Representative Name is the full name of the individual sales person responsible for managing customer relationships and generating booking transactions. This is the primary descriptor used for sales representative identification.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_sales_rep  
**Source Column:** rep_name  
**Data Type:** Character Varying(60)  
**Entity:** [Sales Representative](../entities/sales-representative.md)  
**Attribute:** Sales Representative Name  
**Confidence Score:** 1.00

---

## Related Concepts

- [Sales Representative](./sales-representative.md) - Parent entity
- [Sales Representative ID](./sales-representative-id.md) - Business identifier
- [Sales Representative Key](./sales-representative-key.md) - Surrogate identifier

---

## Usage Context

Sales Representative Name is used to:
- Identify sales personnel in reports and analysis
- Support sales representative search and lookup
- Enable personnel communication
- Provide human-readable sales representative identification

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/sales-representative.md)
- [Return to Bundle Index](../index.md)
