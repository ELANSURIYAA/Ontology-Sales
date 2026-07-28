---
title: Sales Team
type: glossary
description: Team or organizational unit to which the sales representative belongs
resource: glossary
tags: [glossary, sales-rep, team, organization]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Team

## Business Definition

Team or organizational unit to which the sales representative belongs.

---

## Business Meaning

Sales Team identifies the organizational group or team to which the sales representative is assigned. Teams enable collaborative selling, shared accountability, and team-based performance management. Sales teams may be organized by geography, customer segment, product line, or other criteria.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_sales_rep  
**Source Column**: sales_team  
**Entity**: [Sales Representative](../entities/sales-representative.md)  
**Attribute**: Sales Team  
**Data Type**: character varying(40)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Team
- Sales Organization
- Sales Group

---

## Related Concepts

### Related Entities
- [Sales Representative](../entities/sales-representative.md)

### Related Attributes
- [Sales Role](sales-role.md)
- [Covered Segment](covered-segment.md)

---

## Usage Context

Sales Team is used to:
- Organize sales personnel
- Track team performance
- Support team-based compensation
- Enable collaborative selling

---

## Navigation

- [View Glossary Index](index.md)
- [View Sales Representative Entity](../entities/sales-representative.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Sales Representative  
**Source Attribute**: Sales Team  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
