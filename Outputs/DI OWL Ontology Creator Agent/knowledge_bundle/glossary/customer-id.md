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

Customer ID is the business-recognized identifier used to uniquely identify customer accounts in operational systems and business processes. Unlike the surrogate Customer Key, the Customer ID is meaningful to business users and is used in customer communications, account management, and business reporting.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer

**Source Column**: customer_id

**Entity**: [Customer](../entities/customer.md)

**Attribute**: Customer ID

**Data Type**: Character Varying(20)

**Confidence Score**: 1.00

---

## Related Concepts

- [Customer](customer.md)
- [Customer Key](customer-key.md)
- [Customer Name](customer-name.md)

---

## Usage Context

Customer ID is used to:
- Identify customer accounts in business processes
- Support customer lookup and reference
- Enable cross-system customer identification
- Facilitate customer communications
- Support account management operations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Customer](../entities/customer.md)
- [Back to Main Index](../index.md)
