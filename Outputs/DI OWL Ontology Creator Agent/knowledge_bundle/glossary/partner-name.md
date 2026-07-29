---
title: Partner Name
type: glossary
description: Name of the partner organization involved in the transaction
resource: glossary
tags: [partner, name, organization, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Partner Name

## Business Definition

Name of the partner organization involved in the transaction.

---

## Business Meaning

Partner Name is the official name of the organization that facilitates sales transactions. This is the primary descriptor used for partner identification and reporting.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_partner  
**Source Column:** partner_name  
**Data Type:** Character Varying(60)  
**Entity:** [Partner](../entities/partner.md)  
**Attribute:** Partner Name  
**Confidence Score:** 1.00

---

## Related Concepts

- [Partner](./partner.md) - Parent entity
- [Partner ID](./partner-id.md) - Business identifier
- [Partner Key](./partner-key.md) - Surrogate identifier

---

## Usage Context

Partner Name is used to:
- Identify partner organizations in reports and analysis
- Support partner search and lookup
- Enable partner communication and engagement
- Provide human-readable partner identification

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/partner.md)
- [Return to Bundle Index](../index.md)
