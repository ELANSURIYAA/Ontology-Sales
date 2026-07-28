---
title: Customer ID
type: glossary
description: Business identifier assigned to the customer account
resource: glossary
tags: [glossary, customer, identifier, business-key]
timestamp: 2026-07-28T00:00:00Z
---

# Customer ID

## Business Definition

Business identifier assigned to the customer account.

---

## Business Meaning

Customer ID is the business-level identifier used to reference customer accounts in operational systems and business communications. Unlike the surrogate Customer Key, the Customer ID is a meaningful business identifier that may be shared with customers and used in external communications.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_customer  
**Source Column**: customer_id  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Customer ID  
**Data Type**: character varying(20)  
**Nullable**: No  
**Confidence Score**: 1.00

---

## Synonyms

- Account Number
- Customer Number
- Account ID
- Customer Account ID

---

## Related Concepts

### Related Entities
- [Customer](../entities/customer.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Customer Key](customer-key.md)
- [Customer Name](customer-name.md)

---

## Usage Context

Customer ID is used to:
- Identify customer accounts in business operations
- Reference customers in external communications
- Link customer data across systems
- Support customer service and account management

---

## Navigation

- [View Glossary Index](index.md)
- [View Customer Entity](../entities/customer.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Customer  
**Source Attribute**: Customer ID  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
