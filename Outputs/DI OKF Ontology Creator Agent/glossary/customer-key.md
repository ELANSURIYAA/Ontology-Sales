---
title: Customer Key
type: glossary
description: Surrogate key that uniquely identifies a customer record in the customer dimension
resource: glossary
tags: [okf, glossary, attribute, customer, key]
timestamp: 2026-07-28T00:00:00Z
---

# Customer Key

## Business Definition

Surrogate key that uniquely identifies a customer record in the customer dimension.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_customer  
**Source Column**: customer_key  
**Entity**: Customer Dimension  
**Attribute**: Customer Key

---

## Business Meaning

The Customer Key is a system-generated unique identifier used to link booking transactions to their associated customer attributes. It serves as the primary key in the Customer Dimension and as a foreign key in the Booking Fact table.

---

## Related Concepts

- [Customer Dimension](customer-dimension.md)
- [Booking Fact](booking-fact.md)

---

## Navigation

- [Back to Glossary Index](index.md)
- [Back to Bundle Index](../index.md)
