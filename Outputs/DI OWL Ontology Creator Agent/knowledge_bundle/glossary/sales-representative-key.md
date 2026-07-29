---
title: Sales Representative Key
type: glossary
description: Surrogate key that uniquely identifies a sales representative record in the sales representative dimension
resource: glossary
tags: [sales, representative, key, identifier, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative Key

## Business Definition

Surrogate key that uniquely identifies a sales representative record in the sales representative dimension.

---

## Business Meaning

Sales Representative Key is a system-generated unique identifier used to link sales representative records to booking transactions. It serves as the primary key for the sales representative dimension and enables efficient joins in analytical queries.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_sales_rep  
**Source Column:** sales_rep_key  
**Data Type:** Integer  
**Entity:** [Sales Representative](../entities/sales-representative.md)  
**Attribute:** Sales Representative Key  
**Confidence Score:** 1.00

---

## Related Concepts

- [Sales Representative](./sales-representative.md) - Parent entity
- [Booking Transaction](./booking-transaction.md) - Uses sales representative key as foreign key
- [Sales Representative ID](./sales-representative-id.md) - Business identifier

---

## Usage Context

Sales Representative Key is used to:
- Uniquely identify each sales representative record
- Link booking transactions to sales representative attributes
- Enable dimensional analysis by sales representative characteristics
- Support referential integrity in the data model

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/sales-representative.md)
- [Return to Bundle Index](../index.md)
