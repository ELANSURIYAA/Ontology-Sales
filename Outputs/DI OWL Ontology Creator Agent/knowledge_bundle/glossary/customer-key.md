---
title: Customer Key
type: glossary
description: Surrogate key that uniquely identifies a customer record in the customer dimension
resource: glossary
tags: [glossary, customer, key, identifier, surrogate-key]
timestamp: 2026-07-28T00:00:00Z
---

# Customer Key

## Business Definition

Surrogate key that uniquely identifies a customer record in the customer dimension.

---

## Business Meaning

Customer Key is a system-generated unique identifier used to establish relationships between the customer dimension and booking transaction fact records. It serves as the primary key for customer records and enables efficient data integration and referential integrity.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer

**Source Column**: customer_key

**Entity**: [Customer](../entities/customer.md)

**Attribute**: Customer Key

**Data Type**: Integer

**Confidence Score**: 1.00

---

## Related Concepts

- [Customer](customer.md)
- [Booking Transaction](booking-transaction.md)

---

## Usage Context

Customer Key is used to:
- Uniquely identify customer records
- Link booking transactions to customers
- Maintain referential integrity
- Enable efficient joins between fact and dimension tables
- Support data warehouse operations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Customer](../entities/customer.md)
- [Back to Main Index](../index.md)
