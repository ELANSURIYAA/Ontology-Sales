---
title: Sales Representative Key
type: glossary
description: Surrogate key that uniquely identifies a sales representative record in the sales representative dimension
resource: glossary
tags: [glossary, sales-representative, key, identifier, surrogate-key]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative Key

## Business Definition

Surrogate key that uniquely identifies a sales representative record in the sales representative dimension.

---

## Business Meaning

Sales Representative Key is a system-generated unique identifier used to establish relationships between the sales representative dimension and booking transaction fact records. It serves as the primary key for sales representative records and enables efficient data integration and referential integrity.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_sales_rep

**Source Column**: sales_rep_key

**Entity**: [Sales Representative](../entities/sales-representative.md)

**Attribute**: Sales Representative Key

**Data Type**: Integer

**Confidence Score**: 1.00

---

## Related Concepts

- [Sales Representative](sales-representative.md)
- [Booking Transaction](booking-transaction.md)

---

## Usage Context

Sales Representative Key is used to:
- Uniquely identify sales representative records
- Link booking transactions to sales representatives
- Maintain referential integrity
- Enable efficient joins between fact and dimension tables
- Support data warehouse operations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Sales Representative](../entities/sales-representative.md)
- [Back to Main Index](../index.md)
