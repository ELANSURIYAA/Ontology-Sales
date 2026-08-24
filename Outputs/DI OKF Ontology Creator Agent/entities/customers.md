---
title: Customers
type: entity
description: Customer organizations that place orders with segment, industry, and location attributes
resource: entities
tags: [customers, dimension, accounts]
timestamp: 2026-07-28T00:00:00Z
---

# Customers

## Business Definition

Stores descriptive information about customers that place orders, including identity, segment, industry, account tier, and headquarters location.

Customers represent the organizations or accounts that purchase products and services through booking transactions.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_customer

**Source Columns**: customer_key, customer_id, customer_name, segment, industry, account_tier, hq_country, hq_region

---

## Attributes

- **customer_key** - Surrogate key that uniquely identifies a customer record in the customer dimension
- **customer_id** - Business identifier assigned to the customer account
- **customer_name** - Official name of the customer organization
- **segment** - Market segment the customer belongs to, such as Enterprise, Service Provider, or Public Sector
- **industry** - Industry classification of the customer organization
- **account_tier** - Strategic importance or service tier assigned to the customer account
- **hq_country** - Country where the customer organization's headquarters is located
- **hq_region** - Broad geographic region of the customer organization's headquarters

---

## Primary Keys

- customer_key

---

## Foreign Keys

None

---

## Relationships

- [Bookings to Customers](../relationships/bookings-to-customers.md)

---

## Measures

All booking-related measures can be analyzed by customer attributes:
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Booking Count](../measures/booking-count.md)

---

## Related Concepts

- [Customer Segment](../glossary/customer-segment.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

- Each customer must have a unique customer_key
- customer_id serves as the natural business identifier
- Customers can be analyzed by segment, industry, account tier, and geographic location
- Customer attributes enable market segmentation and account profitability analysis

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
