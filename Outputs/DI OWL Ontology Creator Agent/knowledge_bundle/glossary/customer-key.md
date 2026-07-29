---
title: Customer Key
type: glossary
description: Surrogate key that uniquely identifies a customer record in the customer dimension
resource: glossary
tags: [customer, key, identifier, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Customer Key

## Business Definition

Surrogate key that uniquely identifies a customer record in the customer dimension.

---

## Business Meaning

Customer Key is a system-generated unique identifier used to link customer records to booking transactions. It serves as the primary key for the customer dimension and enables efficient joins in analytical queries.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_customer  
**Source Column:** customer_key  
**Data Type:** Integer  
**Entity:** [Customer](../entities/customer.md)  
**Attribute:** Customer Key  
**Confidence Score:** 1.00

---

## Related Concepts

- [Customer](./customer.md) - Parent entity
- [Booking Transaction](./booking-transaction.md) - Uses customer key as foreign key
- [Customer ID](./customer-id.md) - Business identifier

---

## Usage Context

Customer Key is used to:
- Uniquely identify each customer record
- Link booking transactions to customer attributes
- Enable dimensional analysis by customer characteristics
- Support referential integrity in the data model

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/customer.md)
- [Return to Bundle Index](../index.md)
