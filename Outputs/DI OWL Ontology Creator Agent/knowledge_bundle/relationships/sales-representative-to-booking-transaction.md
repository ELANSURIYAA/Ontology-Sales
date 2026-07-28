---
title: Sales Representative to Booking Transaction
type: relationship
description: One-to-Many relationship linking sales representatives to booking transactions
resource: relationships
tags: [relationship, foreign-key, sales-representative, booking-transaction, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative to Booking Transaction

## Business Description

This relationship links sales representative records to booking transactions, enabling analysis of bookings by sales representative, sales role, sales team, and covered segment.

---

## Relationship Details

**Source Entity**: [Sales Representative](../entities/sales-representative.md)

**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Relationship Type**: Foreign Key

**Cardinality**: One-to-Many

**Confidence Score**: 1.00

---

## Technical Mapping

**Parent Table**: QuoteToBooking.dim_sales_rep

**Parent Column**: sales_rep_key

**Child Table**: QuoteToBooking.fact_bookings

**Child Column**: sales_rep_key

---

## Cardinality Explanation

- **One Sales Representative** can be associated with **Many Booking Transactions**
- **Each Booking Transaction** must reference **exactly one Sales Representative**

This relationship enables:
- Analysis of booking amounts by sales representative
- Evaluation of sales role performance
- Measurement of sales team effectiveness
- Individual and team quota attainment tracking

---

## Business Rules

1. Every booking transaction must reference a valid sales representative
2. A sales representative can be associated with zero or many booking transactions
3. Sales Representative Key is the foreign key in the booking transaction fact table
4. The relationship is mandatory on the booking transaction side
5. The relationship supports referential integrity

---

## Related Concepts

- [Sales Representative](../glossary/sales-representative.md)
- [Sales Representative Key](../glossary/sales-representative-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Sales Role](../glossary/sales-role.md)
- [Sales Team](../glossary/sales-team.md)
- [Covered Segment](../glossary/covered-segment.md)

---

## Usage Examples

**Analyze bookings by sales representative**:
- Identify top-performing sales representatives
- Measure individual quota attainment

**Analyze bookings by sales role**:
- Compare performance across different sales roles
- Evaluate role effectiveness

**Analyze bookings by sales team**:
- Measure team performance and contribution
- Compare team results across geographies

**Sales performance management**:
- Track individual and team productivity
- Analyze average deal size by sales representative
- Measure sales cycle effectiveness

---

## Navigation

- [Back to Relationships Index](index.md)
- [View Source Entity: Sales Representative](../entities/sales-representative.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
