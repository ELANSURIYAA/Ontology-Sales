---
title: Customer Name
type: glossary
description: Official name of the customer organization that purchased products or services
resource: glossary
tags: [glossary, customer, name, organization]
timestamp: 2026-07-28T00:00:00Z
---

# Customer Name

## Business Definition

Official name of the customer organization that purchased products or services.

---

## Business Meaning

Customer Name is the legal or commonly used business name of the customer organization. This name is used for reporting, communications, and business analysis. It provides human-readable identification of customer accounts.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_customer  
**Source Column**: customer_name  
**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Customer Name  
**Data Type**: character varying(80)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Account Name
- Organization Name
- Company Name
- Customer Organization Name

---

## Related Concepts

### Related Entities
- [Customer](../entities/customer.md)

### Related Attributes
- [Customer Key](customer-key.md)
- [Customer ID](customer-id.md)

---

## Usage Context

Customer Name is used to:
- Identify customers in reports and dashboards
- Support customer communications
- Enable customer search and lookup
- Provide human-readable customer identification

---

## Navigation

- [View Glossary Index](index.md)
- [View Customer Entity](../entities/customer.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Customer  
**Source Attribute**: Customer Name  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
