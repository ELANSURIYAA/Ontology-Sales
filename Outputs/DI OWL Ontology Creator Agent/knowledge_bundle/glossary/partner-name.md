---
title: Partner Name
type: glossary
description: Name of the partner organization involved in the transaction
resource: glossary
tags: [glossary, partner, name, organization]
timestamp: 2026-07-28T00:00:00Z
---

# Partner Name

## Business Definition

Name of the partner organization involved in the transaction.

---

## Business Meaning

Partner Name is the legal or commonly used business name of the partner organization. This name is used for reporting, communications, and business analysis. It provides human-readable identification of partner accounts.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_partner  
**Source Column**: partner_name  
**Entity**: [Partner](../entities/partner.md)  
**Attribute**: Partner Name  
**Data Type**: character varying(60)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Partner Organization Name
- Partner Company Name

---

## Related Concepts

### Related Entities
- [Partner](../entities/partner.md)

### Related Attributes
- [Partner Key](partner-key.md)
- [Partner ID](partner-id.md)

---

## Usage Context

Partner Name is used to:
- Identify partners in reports and dashboards
- Support partner communications
- Enable partner search and lookup

---

## Navigation

- [View Glossary Index](index.md)
- [View Partner Entity](../entities/partner.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Partner  
**Source Attribute**: Partner Name  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
