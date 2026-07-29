---
title: Sales Representative Dimension
type: entity
description: Sales representative attributes used to analyze bookings by seller, role, team, and segment coverage
resource: entities
tags: [okf, entity, sales-rep, dimension, sales-organization]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative Dimension

## Business Definition

The Sales Representative Dimension stores sales representative attributes used to analyze bookings by sales person, role, team, and market segment coverage. This dimension enables sales performance management and supports territory analytics.

---

## Technical Mapping

**Source Schema**: quotetobooking  
**Source Table**: dim_sales_rep  
**Entity Type**: Dimension  
**Grain**: One record per unique sales representative

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

None (this is a dimension table)

---

## Relationships

### Outbound Relationships
- [Sales Representative to Booking](../relationships/sales-representative-to-booking.md) - One-to-Many relationship to Booking Fact

---

## Measures

All booking measures can be analyzed by sales representative attributes:

- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Related Concepts

### Related Entities
- [Booking Fact](booking-fact.md)

### Related Domains
- [Sales Organization](../domains/sales-organization.md)
- [Sales Transactions](../domains/sales-transactions.md)

### Related Glossary Terms
- [Sales Representative Dimension](../glossary/sales-representative-dimension.md)
- [Sales Representative Key](../glossary/sales-representative-key.md)
- [Sales Representative ID](../glossary/sales-representative-id.md)
- [Sales Representative Name](../glossary/sales-representative-name.md)
- [Sales Role](../glossary/sales-role.md)
- [Sales Team](../glossary/sales-team.md)
- [Segment Covered](../glossary/segment-covered.md)

---

## Business Rules

1. Sales Representative Key must be unique and not null
2. Sales Representative ID must be unique and not null
3. Sales Representative Name is required for all records
4. Sales Role should be populated for all representatives
5. Sales Team should be populated for all representatives
6. Segment Covered should align with customer segment classifications

---

## Attribute Details

### sales_rep_key
- **Data Type**: integer
- **Nullable**: No
- **Primary Key**: Yes
- **Description**: Surrogate key that uniquely identifies a sales representative record in the sales representative dimension

### rep_id
- **Data Type**: character varying(20)
- **Nullable**: No
- **Description**: Business identifier assigned to the sales representative

### rep_name
- **Data Type**: character varying(60)
- **Nullable**: Yes
- **Description**: Full name of the sales representative managing the account or opportunity

### sales_role
- **Data Type**: character varying(40)
- **Nullable**: Yes
- **Description**: Job role or selling role performed by the sales representative

### sales_team
- **Data Type**: character varying(40)
- **Nullable**: Yes
- **Description**: Sales team or organization to which the representative belongs

### segment_covered
- **Data Type**: character varying(30)
- **Nullable**: Yes
- **Description**: Customer segment primarily covered by the sales representative

---

## Analytical Use Cases

- Analyze sales performance by sales representative
- Track revenue by sales role and team
- Monitor quota attainment and productivity
- Evaluate segment coverage effectiveness
- Support sales capacity planning
- Measure sales representative contribution

---

## Data Quality Metrics

- **Completeness**: Sales Representative Key and ID must be 100% populated
- **Uniqueness**: Sales Representative Key and ID must be unique
- **Validity**: Sales Role and Segment Covered must match approved values
- **Consistency**: Sales Team must align with organizational structure

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Bundle Index](../index.md)
