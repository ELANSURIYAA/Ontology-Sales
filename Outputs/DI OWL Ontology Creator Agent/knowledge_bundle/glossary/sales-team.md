---
title: Sales Team
type: glossary
description: Team or organizational unit to which the sales representative belongs
resource: glossary
tags: [sales, representative, team, organization, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Team

## Business Definition

Team or organizational unit to which the sales representative belongs.

---

## Business Meaning

Sales Team identifies the organizational unit or team structure to which the sales representative is assigned. This classification enables team-based performance analysis and supports organizational reporting.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_sales_rep  
**Source Column:** sales_team  
**Data Type:** Character Varying(40)  
**Entity:** [Sales Representative](../entities/sales-representative.md)  
**Attribute:** Sales Team  
**Confidence Score:** 1.00

---

## Related Concepts

- [Sales Representative](./sales-representative.md) - Parent entity
- [Sales Role](./sales-role.md) - Job role
- [Covered Segment](./covered-segment.md) - Segment responsibility

---

## Usage Context

Sales Team is used to:
- Identify team affiliation and organizational structure
- Enable team-based performance analysis
- Support team management and reporting
- Track team contribution and effectiveness

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/sales-representative.md)
- [Return to Bundle Index](../index.md)
