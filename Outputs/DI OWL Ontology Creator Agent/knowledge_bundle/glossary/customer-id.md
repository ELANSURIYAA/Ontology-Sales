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

## Business Meaning

Customer ID is the business-facing identifier used to reference customer accounts in operational systems, reports, and communications. Unlike the surrogate Customer Key, the Customer ID is meaningful to business users and is used in customer-facing contexts.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer  
**Source Column**: customer_id  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Customer ID  
**Data Type**: Character Varying(20)  
**Confidence Score**: 1.00

## Synonyms

- Account ID
- Customer Number
- Account Number

## Related Concepts

- [Customer](./customer.md)
- [Customer Key](./customer-key.md)
- [Customer Name](./customer-name.md)

## Usage Context

Customer ID is used to:
- Reference customer accounts in business communications
- Look up customer information
- Integrate with external systems
- Support customer service and account management

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Customer (ENT002)  
**Attribute**: ATTR007
