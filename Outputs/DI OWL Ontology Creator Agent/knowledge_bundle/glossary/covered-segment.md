---
title: Covered Segment
type: glossary
description: Customer segment for which the sales representative is responsible
resource: glossary
tags: [sales, representative, segment, coverage, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Covered Segment

## Business Definition

Customer segment for which the sales representative is responsible.

---

## Business Meaning

Covered Segment identifies the customer segment that the sales representative is assigned to manage and serve. This classification enables segment-based sales coverage analysis and territory management.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_sales_rep  
**Source Column:** segment_covered  
**Data Type:** Character Varying(30)  
**Entity:** [Sales Representative](../entities/sales-representative.md)  
**Attribute:** Covered Segment  
**Confidence Score:** 1.00

---

## Related Concepts

- [Sales Representative](./sales-representative.md) - Parent entity
- [Customer Segment](./customer-segment.md) - Customer classification
- [Sales Role](./sales-role.md) - Job role
- [Sales Team](./sales-team.md) - Team affiliation

---

## Usage Context

Covered Segment is used to:
- Identify sales representative segment responsibilities
- Enable segment coverage analysis
- Support territory and account assignment
- Track segment-specific sales performance

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/sales-representative.md)
- [Return to Bundle Index](../index.md)
