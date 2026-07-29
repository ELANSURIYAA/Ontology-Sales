---
title: Customer Key
type: glossary
description: Surrogate key that uniquely identifies a customer record in the customer dimension
resource: glossary
tags: [glossary, customer, key, identifier]
timestamp: 2026-07-28T00:00:00Z
---

# Customer Key

## Business Definition

Surrogate key that uniquely identifies a customer record in the customer dimension.

## Business Meaning

The Customer Key is a system-generated unique identifier used to link customer dimension records to booking transaction fact records. It serves as the primary key for the customer dimension and enables efficient joins and referential integrity in the dimensional model.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer  
**Source Column**: customer_key  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Customer Key  
**Data Type**: Integer  
**Confidence Score**: 1.00

## Synonyms

- Customer Identifier
- Customer Surrogate Key
- Account Key

## Related Concepts

- [Customer](./customer.md)
- [Booking Transaction](./booking-transaction.md)

## Usage Context

The Customer Key is used to:
- Uniquely identify customer records
- Link customers to booking transactions
- Maintain referential integrity
- Enable efficient dimensional queries

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Customer (ENT002)  
**Attribute**: ATTR006
