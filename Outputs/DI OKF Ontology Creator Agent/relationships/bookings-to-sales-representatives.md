---
title: Bookings to Sales Representatives
type: relationship
description: Links booking transactions to sales representatives
resource: relationships
tags: [bookings, sales-representatives, many-to-one, relationship]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Sales Representatives

## Business Definition

The Bookings to Sales Representatives relationship links individual booking transactions to the sales personnel responsible for managing customer relationships and closing deals. This relationship enables analysis of booking performance by sales role, sales team, and segment coverage, supporting sales performance management and territory optimization.

---

## Relationship Type

**Many-to-one**

Multiple booking transactions can be associated with the same sales representative.

---

## Source Entity

**[Bookings](../entities/bookings.md)**

The fact table containing individual completed sales booking transactions.

---

## Target Entity

**[Sales Representatives](../entities/sales-representatives.md)**

The dimension table containing sales representative information.

---

## Cardinality

**Many Bookings : One Sales Representative**

- Each booking transaction references exactly one sales representative record
- Multiple booking transactions can be associated with the same sales representative
- Sales representative records can exist without associated bookings

---

## Join Specification

### Left Join Key
- **Field**: sales_rep_key
- **Entity**: Bookings
- **Type**: Foreign Key

### Right Join Key
- **Field**: sales_rep_key
- **Entity**: Sales Representatives
- **Type**: Primary Key

### Join Condition
```sql
bookings.sales_rep_key = sales_representatives.sales_rep_key
```

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings

**Target Table**: quotetobooking.dim_sales_rep

**Join Column**: sales_rep_key

---

## Business Purpose

This relationship enables:

- **Sales Role Analysis**: Analyze booking performance by sales role
- **Sales Team Analysis**: Track team-level performance and contribution
- **Segment Coverage Analysis**: Evaluate sales effectiveness by segment coverage
- **Individual Performance**: Rank sales representatives by booking contribution
- **Quota Attainment**: Track individual and team quota achievement
- **Territory Optimization**: Optimize territory assignments and coverage

---

## Related Measures

All booking measures can be analyzed by sales representative attributes:
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

1. **Mandatory Relationship**: Every booking must reference a valid sales representative
2. **Referential Integrity**: sales_rep_key in bookings must exist in sales_representatives dimension
3. **One Sales Rep per Booking**: Each booking references exactly one sales representative record
4. **Sales Rep Independence**: Sales representatives can exist without bookings (new hires, inactive reps)

---

## Usage Examples

### Sales Role Analysis
```sql
SELECT 
    sales_representatives.sales_role,
    COUNT(bookings.booking_id) as booking_count,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN sales_representatives ON bookings.sales_rep_key = sales_representatives.sales_rep_key
GROUP BY sales_representatives.sales_role
```

### Top Performers Analysis
```sql
SELECT 
    sales_representatives.rep_name,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN sales_representatives ON bookings.sales_rep_key = sales_representatives.sales_rep_key
GROUP BY sales_representatives.rep_name
ORDER BY total_booking_amount DESC
LIMIT 10
```

---

## Data Quality Rules

- sales_rep_key in bookings must not be null
- sales_rep_key in bookings must reference valid sales_rep_key in sales_representatives
- No orphaned bookings without sales representative references
- Sales representative dimension must be populated before booking transactions

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
