---
title: Customer Name
type: glossary
description: Official name of the customer organization that purchased products or services
resource: glossary
tags: [customer, name, organization, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Customer Name

## Business Definition

Official name of the customer organization that purchased products or services.

---

## Business Meaning

Customer Name is the legal or official name of the organization that enters into commercial agreements and generates booking transactions. This is the primary descriptor used for customer identification and reporting.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_customer  
**Source Column:** customer_name  
**Data Type:** Character Varying(80)  
**Entity:** [Customer](../entities/customer.md)  
**Attribute:** Customer Name  
**Confidence Score:** 1.00

---

## Related Concepts

- [Customer](./customer.md) - Parent entity
- [Customer ID](./customer-id.md) - Business identifier
- [Customer Key](./customer-key.md) - Surrogate identifier

---

## Usage Context

Customer Name is used to:
- Identify customer organizations in reports and analysis
- Support customer search and lookup
- Enable customer communication and engagement
- Provide human-readable customer identification

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/customer.md)
- [Return to Bundle Index](../index.md)
