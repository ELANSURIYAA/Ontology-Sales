---
title: Covered Segment
type: glossary
description: Customer segment for which the sales representative is responsible
resource: glossary
tags: [glossary, sales-rep, segment, territory]
timestamp: 2026-07-28T00:00:00Z
---

# Covered Segment

## Business Definition

Customer segment for which the sales representative is responsible.

---

## Business Meaning

Covered Segment identifies the customer segment or market segment assigned to the sales representative. This assignment defines the sales representative's territory or coverage area and enables segment-based performance tracking and territory management.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_sales_rep  
**Source Column**: segment_covered  
**Entity**: [Sales Representative](../entities/sales-representative.md)  
**Attribute**: Covered Segment  
**Data Type**: character varying(30)  
**Nullable**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Territory Segment
- Assigned Segment
- Coverage Segment

---

## Related Concepts

### Related Entities
- [Sales Representative](../entities/sales-representative.md)
- [Customer](../entities/customer.md)

### Related Attributes
- [Sales Role](sales-role.md)
- [Sales Team](sales-team.md)
- [Customer Segment](customer-segment.md)

---

## Usage Context

Covered Segment is used to:
- Define sales territories
- Track segment coverage
- Analyze performance by assigned segment
- Support territory planning

---

## Examples

- Enterprise
- Service Provider
- Public Sector
- Mid-Market

---

## Navigation

- [View Glossary Index](index.md)
- [View Sales Representative Entity](../entities/sales-representative.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Sales Representative  
**Source Attribute**: Covered Segment  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
