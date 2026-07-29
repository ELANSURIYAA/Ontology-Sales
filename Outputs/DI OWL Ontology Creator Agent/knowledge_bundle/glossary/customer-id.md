---
title: Customer ID
type: glossary
description: Business identifier assigned to the customer account
resource: glossary
tags: [customer, identifier, business-key, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Customer ID

## Business Definition

Business identifier assigned to the customer account.

---

## Business Meaning

Customer ID is the business-recognized identifier used to reference customer accounts in operational systems and business communications. Unlike the surrogate Customer Key, this is a meaningful business identifier.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_customer  
**Source Column:** customer_id  
**Data Type:** Character Varying(20)  
**Entity:** [Customer](../entities/customer.md)  
**Attribute:** Customer ID  
**Confidence Score:** 1.00

---

## Related Concepts

- [Customer](./customer.md) - Parent entity
- [Customer Key](./customer-key.md) - Surrogate identifier
- [Customer Name](./customer-name.md) - Organization name

---

## Usage Context

Customer ID is used to:
- Reference customer accounts in business processes
- Integrate with operational systems
- Support customer lookup and identification
- Enable cross-system customer tracking

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/customer.md)
- [Return to Bundle Index](../index.md)
