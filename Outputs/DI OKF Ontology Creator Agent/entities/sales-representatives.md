---
title: Sales Representatives
type: entity
description: Sales personnel managing customer relationships with role, team, and segment coverage attributes
resource: entities
tags: [sales-representatives, dimension, personnel]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representatives

## Business Definition

Stores information about the sales person responsible for managing customer relationships and booking transactions, including role, team, and segment coverage.

Sales representatives are the individuals who drive sales activities and are accountable for booking performance.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_sales_rep

**Source Columns**: sales_rep_key, rep_id, rep_name, sales_role, sales_team, segment_covered

---

## Attributes

- **sales_rep_key** - Surrogate key that uniquely identifies a sales representative record in the sales representative dimension
- **rep_id** - Business identifier assigned to the sales representative
- **rep_name** - Full name of the sales representative
- **sales_role** - Job role or selling responsibility of the sales representative
- **sales_team** - Team or organizational unit the sales representative belongs to
- **segment_covered** - Customer segment or market segment covered by the sales representative

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

All booking-related measures can be analyzed by sales representative attributes:
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

---

## Related Concepts

- [Customer Segment](../glossary/customer-segment.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

- Each sales representative must have a unique sales_rep_key
- rep_id serves as the natural business identifier
- Sales representatives are organized by role, team, and segment coverage
- segment_covered aligns sales representatives with customer segments
- Sales performance can be tracked by individual representative, role, team, and segment
- Enables sales productivity and quota attainment analysis

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
