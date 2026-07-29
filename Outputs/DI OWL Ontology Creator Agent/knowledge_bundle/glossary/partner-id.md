---
title: Partner ID
type: glossary
description: Business identifier assigned to the partner organization
resource: glossary
tags: [glossary, partner, identifier, business-key]
timestamp: 2026-07-28T00:00:00Z
---

# Partner ID

## Business Definition

Business identifier assigned to the partner organization.

## Business Meaning

Partner ID is the business-facing identifier used to reference partner organizations in operational systems, reports, and communications. It is used in partner-facing contexts and partner management activities.

## Technical Mapping

**Source Table**: QuoteToBooking.dim_partner  
**Source Column**: partner_id  
**Entity**: [Partner](../entities/partner.md)  
**Attribute**: Partner ID  
**Data Type**: Character Varying(20)  
**Confidence Score**: 1.00

## Synonyms

- Partner Number
- Partner Code

## Related Concepts

- [Partner](./partner.md)
- [Partner Key](./partner-key.md)
- [Partner Name](./partner-name.md)

## Usage Context

Partner ID is used to:
- Reference partners in business communications
- Look up partner information
- Integrate with partner systems
- Support partner management

---

**Confidence Score**: 1.00  
**Source**: OSI Semantic Model  
**Entity**: Partner (ENT005)  
**Attribute**: ATTR026
