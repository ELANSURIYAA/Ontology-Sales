---
title: Sales Representative Key
type: glossary
description: Surrogate key that uniquely identifies a sales representative record in the sales representative dimension
resource: glossary
tags: [okf, glossary, attribute, sales-rep, key]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative Key

## Business Definition

Surrogate key that uniquely identifies a sales representative record in the sales representative dimension.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_sales_rep  
**Source Column**: sales_rep_key  
**Entity**: Sales Representative Dimension  
**Attribute**: Sales Representative Key

---

## Business Meaning

The Sales Representative Key is a system-generated unique identifier used to link booking transactions to their associated sales representative attributes. It serves as the primary key in the Sales Representative Dimension and as a foreign key in the Booking Fact table.

---

## Related Concepts

- [Sales Representative Dimension](sales-representative-dimension.md)
- [Booking Fact](booking-fact.md)

---

## Navigation

- [Back to Glossary Index](index.md)
- [Back to Bundle Index](../index.md)
