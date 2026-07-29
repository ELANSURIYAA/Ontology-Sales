---
title: Partner ID
type: glossary
description: Business identifier assigned to the partner organization
resource: glossary
tags: [partner, identifier, business-key, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Partner ID

## Business Definition

Business identifier assigned to the partner organization.

---

## Business Meaning

Partner ID is the business-recognized identifier used to reference partner organizations in operational systems and business communications. Unlike the surrogate Partner Key, this is a meaningful business identifier.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_partner  
**Source Column:** partner_id  
**Data Type:** Character Varying(20)  
**Entity:** [Partner](../entities/partner.md)  
**Attribute:** Partner ID  
**Confidence Score:** 1.00

---

## Related Concepts

- [Partner](./partner.md) - Parent entity
- [Partner Key](./partner-key.md) - Surrogate identifier
- [Partner Name](./partner-name.md) - Organization name

---

## Usage Context

Partner ID is used to:
- Reference partner organizations in business processes
- Integrate with operational systems
- Support partner lookup and identification
- Enable cross-system partner tracking

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/partner.md)
- [Return to Bundle Index](../index.md)
