---
title: Sales Representatives
type: entity
description: Stores information about the sales person responsible for managing customer relationships and booking transactions, including role, team, and segment coverage
resource: entities
tags: [sales-representatives, dimension, sales-team, sales-role]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representatives

## Business Definition

The Sales Representatives entity represents the dimension table that stores information about sales personnel responsible for managing customer relationships and booking transactions. Each record contains sales representative identity attributes, role classifications, team assignments, and segment coverage designations. This entity enables analysis of booking transactions by sales representative characteristics and supports sales performance management.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_sales_rep

**Source Schema**: quotetobooking

**Entity Type**: Dimension Table

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

All booking-related measures can be analyzed by sales representative attributes:
- [Booking Count](../measures/booking-count.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

---

## Related Concepts

- [Booking Transaction](../glossary/booking-transaction.md)
- [Customer Segment](../glossary/customer-segment.md)

---

## Business Rules

1. **Unique Sales Rep Key**: Each sales representative record must have a unique sales_rep_key
2. **Representative Identifier**: rep_id represents the business identifier for the sales representative
3. **Sales Role Classification**: Sales representatives are classified by job role or selling responsibility
4. **Team Assignment**: Sales representatives are assigned to teams or organizational units
5. **Segment Coverage**: Sales representatives are assigned to cover specific customer segments or market segments

---

## Attribute Definitions

### sales_rep_key
Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. Used as the primary key and referenced by the bookings fact table.

### rep_id
Business identifier assigned to the sales representative. Represents the natural key used in operational systems.

### rep_name
Full name of the sales representative. Used for reporting and sales representative identification.

### sales_role
Job role or selling responsibility of the sales representative. Enables role-based analysis and performance tracking.

### sales_team
Team or organizational unit the sales representative belongs to. Used for team-level reporting and management.

### segment_covered
Customer segment or market segment covered by the sales representative. Enables segment-based territory analysis and alignment.

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Usage Examples

### Sales Role Analysis
- Analyze booking amount by sales role
- Compare performance across different roles
- Track role-specific productivity metrics

### Sales Team Analysis
- Evaluate team performance and contribution
- Track team-level booking trends
- Support team-based incentive programs

### Segment Coverage Analysis
- Analyze sales representative effectiveness by segment
- Ensure proper segment coverage and alignment
- Optimize territory assignments

### Sales Representative Performance
- Rank sales representatives by booking amount
- Track individual quota attainment
- Identify top performers and coaching opportunities

---

## Data Quality Checks

- sales_rep_key is unique and not null
- rep_id is not null
- rep_name is not null
- sales_role is a valid role classification
- sales_team is a valid team designation
- segment_covered is a valid segment classification
