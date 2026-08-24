---
title: Customer Segment
type: glossary
description: Market segment classification such as Enterprise, Service Provider, or Public Sector
resource: glossary
tags: [customer-segment, segmentation, market]
timestamp: 2026-07-28T00:00:00Z
---

# Customer Segment

## Business Definition

Customer Segment is a market segment classification that groups customers based on their business characteristics, size, industry focus, or organizational type. Common segments include Enterprise, Service Provider, and Public Sector.

---

## Business Meaning

Customer Segment is used to:
- Categorize customers for targeted marketing and sales strategies
- Tailor product offerings and pricing to segment needs
- Allocate sales resources and territories
- Analyze performance by market segment
- Support segment-specific go-to-market strategies
- Enable competitive positioning by segment

Typical customer segments include:
- **Enterprise**: Large commercial organizations
- **Service Provider**: Telecommunications and service companies
- **Public Sector**: Government and public institutions
- **Small/Medium Business**: SMB customers
- **Commercial**: General commercial accounts

---

## Technical Mapping

**Source Entity**: [Customers](../entities/customers.md)

**Source Field**: segment

---

## Synonyms

- Market Segment
- Customer Category
- Customer Type
- Business Segment
- Account Segment

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Transactions analyzed by segment

---

## Related Entities

- [Customers](../entities/customers.md) - Contains segment classification
- [Sales Representatives](../entities/sales-representatives.md) - May be assigned to specific segments

---

## Related Measures

All booking measures can be analyzed by customer segment:
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Total ACV USD](../measures/total-acv-usd.md)

---

## Usage Context

Customer Segment is used for:
- Sales territory planning and assignment
- Targeted marketing campaigns
- Product development and positioning
- Pricing strategy by segment
- Competitive analysis
- Revenue forecasting by segment
- Resource allocation

---

## Business Rules

1. Each customer is assigned to exactly one primary segment
2. Segment classification is based on customer characteristics
3. Segment values are standardized across the organization
4. Segment assignment may change over time as customers evolve

---

## Segmentation Criteria

Segments are typically defined based on:
- Company size (revenue, employees)
- Industry vertical
- Organizational type (commercial, government)
- Business model (service provider, end user)
- Geographic scope (global, regional, local)

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
