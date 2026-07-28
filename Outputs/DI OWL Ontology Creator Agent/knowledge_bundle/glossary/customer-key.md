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

Customer Key is a system-generated unique identifier used to link customer records to booking transactions. It serves as the primary key for the customer dimension and enables efficient joins and referential integrity in the data model.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_customer  
**Source Column**: customer_key  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Customer Key  
**Data Type**: integer  
**Nullable**: No  
**Primary Key**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Customer Identifier
- Customer Surrogate Key
- Customer Record ID

---

## Related Concepts

### Related Entities
- [Customer](../entities/customer.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Relationships
- [Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)

---

## Usage Context

Customer Key is used to:
- Uniquely identify customer records
- Link booking transactions to customers
- Enable dimensional analysis by customer attributes
- Maintain referential integrity

---

## Navigation

- [View Glossary Index](index.md)
- [View Customer Entity](../entities/customer.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Customer  
**Source Attribute**: Customer Key  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
