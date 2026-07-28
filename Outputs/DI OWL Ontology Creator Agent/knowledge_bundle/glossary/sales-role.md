---
title: Sales Role
type: glossary
description: Job role or account responsibility of the sales representative
resource: glossary
tags: [glossary, sales-rep, role, responsibility]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Role

## Business Definition

Job role or account responsibility of the sales representative.

---

## Business Meaning

Sales Role describes the functional role or job title of the sales representative, such as Account Executive, Account Manager, or Territory Manager. This classification enables analysis of performance by role type and supports organizational planning and resource allocation.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_sales_rep  
**Source Column**: sales_role  
**Entity**: [Sales Representative](../entities/sales-representative.md)  
**Attribute**: Sales Role  
**Data Type**: character varying(40)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Job Role
- Position
- Sales Position

---

## Related Concepts

### Related Entities
- [Sales Representative](../entities/sales-representative.md)

### Related Attributes
- [Sales Team](sales-team.md)
- [Covered Segment](covered-segment.md)

---

## Usage Context

Sales Role is used to:
- Classify sales personnel by function
- Analyze performance by role type
- Support organizational planning
- Guide compensation and quota setting

---

## Examples

- Account Executive
- Account Manager
- Territory Manager
- Inside Sales Representative

---

## Navigation

- [View Glossary Index](index.md)
- [View Sales Representative Entity](../entities/sales-representative.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Sales Representative  
**Source Attribute**: Sales Role  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
