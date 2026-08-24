---
title: Bookings to Sales Representatives
type: relationship
description: Links booking transactions to sales personnel
resource: relationships
tags: [bookings, sales-representatives, relationship, many-to-one]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Sales Representatives

## Business Definition

Links booking transactions to the sales person responsible for managing customer relationships and booking transactions, including role, team, and segment coverage.

This relationship enables analysis of sales representative performance and supports sales productivity, quota attainment, and compensation analysis.

---

## Relationship Type

**many-to-one**

Multiple booking transactions can be associated with the same sales representative.

---

## Source Entity

[Bookings](../entities/bookings.md)

---

## Target Entity

[Sales Representatives](../entities/sales-representatives.md)

---

## Cardinality

- Each booking transaction must be associated with exactly one sales representative record
- Each sales representative record can be associated with multiple booking transactions

---

## Technical Mapping

**Join Condition**: bookings.sales_rep_key = sales_representatives.sales_rep_key

**Left Dataset**: bookings (quotetobooking.fact_bookings)

**Right Dataset**: sales_representatives (quotetobooking.dim_sales_rep)

**Join Keys**:
- Left: sales_rep_key
- Right: sales_rep_key

---

## Business Purpose

This relationship enables:
- Individual sales representative performance tracking
- Sales role and team performance analysis
- Segment coverage effectiveness analysis
- Sales productivity and efficiency metrics
- Quota attainment and target achievement tracking
- Sales compensation and incentive analysis

---

## Related Measures

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

---

## Related Concepts

- [Customer Segment](../glossary/customer-segment.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [Return to Relationships Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
