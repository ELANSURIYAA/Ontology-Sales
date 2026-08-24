---
title: Bookings to Customers
type: relationship
description: Links booking transactions to customer organizations
resource: relationships
tags: [bookings, customers, relationship, many-to-one]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Customers

## Business Definition

Links booking transactions to customer organizations that place orders, including customer identity, segment, industry, account tier, and headquarters location.

This relationship enables analysis of booking performance by customer characteristics and supports customer profitability and segmentation analysis.

---

## Relationship Type

**many-to-one**

Multiple booking transactions can be associated with the same customer.

---

## Source Entity

[Bookings](../entities/bookings.md)

---

## Target Entity

[Customers](../entities/customers.md)

---

## Cardinality

- Each booking transaction must be associated with exactly one customer record
- Each customer record can be associated with multiple booking transactions

---

## Technical Mapping

**Join Condition**: bookings.customer_key = customers.customer_key

**Left Dataset**: bookings (quotetobooking.fact_bookings)

**Right Dataset**: customers (quotetobooking.dim_customer)

**Join Keys**:
- Left: customer_key
- Right: customer_key

---

## Business Purpose

This relationship enables:
- Analysis of bookings by customer segment (Enterprise, Service Provider, Public Sector)
- Industry-based performance analysis
- Account tier and strategic customer analysis
- Geographic analysis by customer headquarters location
- Customer profitability and lifetime value analysis

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
