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

---

## Business Meaning

Partner ID is the business-level identifier used to reference partner organizations in operational systems and business communications. Unlike the surrogate Partner Key, the Partner ID is a meaningful business identifier used in partner management and external communications.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_partner  
**Source Column**: partner_id  
**Entity**: [Partner](../entities/partner.md)  
**Attribute**: Partner ID  
**Data Type**: character varying(20)  
**Nullable**: No  
**Confidence Score**: 1.00

---

## Synonyms

- Partner Number
- Partner Account ID

---

## Related Concepts

### Related Entities
- [Partner](../entities/partner.md)

### Related Attributes
- [Partner Key](partner-key.md)
- [Partner Name](partner-name.md)

---

## Usage Context

Partner ID is used to:
- Identify partner organizations in business operations
- Reference partners in external communications
- Link partner data across systems

---

## Navigation

- [View Glossary Index](index.md)
- [View Partner Entity](../entities/partner.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Partner  
**Source Attribute**: Partner ID  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
