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

Partner ID is the business-recognized identifier used to uniquely identify partner organizations in operational systems and business processes. Unlike the surrogate Partner Key, the Partner ID is meaningful to business users and is used in partner communications, program management, and business reporting.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_partner

**Source Column**: partner_id

**Entity**: [Partner](../entities/partner.md)

**Attribute**: Partner ID

**Data Type**: Character Varying(20)

**Confidence Score**: 1.00

---

## Related Concepts

- [Partner](partner.md)
- [Partner Key](partner-key.md)
- [Partner Name](partner-name.md)

---

## Usage Context

Partner ID is used to:
- Identify partner organizations in business processes
- Support partner lookup and reference
- Enable cross-system partner identification
- Facilitate partner communications
- Support partner program operations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Partner](../entities/partner.md)
- [Back to Main Index](../index.md)
