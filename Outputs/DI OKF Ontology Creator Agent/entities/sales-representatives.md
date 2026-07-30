---
title: Sales Representative
type: entity
description: Sales persons responsible for managing customer relationships and booking transactions, including role, team, and segment coverage
resource: entities
tags: [sales-rep, sales-team, seller, performance, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Sales Representative

## Business Definition

The Sales Representative entity stores information about the sales person responsible for managing customer relationships and booking transactions, including role, team, and segment coverage. This entity enables sales performance analysis and quota management.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_sales_rep  
**Source Schema**: quotetobooking  
**Entity Type**: Dimension  
**Grain**: One row per sales representative

---

## Attributes

- sales_rep_key
- rep_id
- rep_name
- sales_role
- sales_team
- segment_covered

---

## Primary Keys

- sales_rep_key

---

## Foreign Keys

None

---

## Relationships

- [Bookings to Sales Representatives](../relationships/bookings-to-sales-representatives.md)

---

## Measures

All booking and revenue measures can be analyzed by sales representative attributes:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

---

## Related Concepts

- [Sales Role](../glossary/sales-role.md)
- [Sales Team](../glossary/sales-team.md)
- [Segment Covered](../glossary/segment-covered.md)

---

## Business Rules

### Sales Representative Identification
Each sales representative is uniquely identified by sales_rep_key (surrogate key) and rep_id (business key).

### Sales Role Assignment
Sales role represents the job role or selling responsibility such as Account Executive or Sales Engineer.

### Sales Team Membership
Sales team represents the team or organizational unit the sales representative belongs to.

### Segment Coverage
Segment covered represents the customer segment or market segment assigned to the sales representative.

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Sales Representatives Domain](../domains/sales-representatives.md)
