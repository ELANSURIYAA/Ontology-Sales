---
title: Sales Representative
type: entity
description: Sales personnel responsible for managing customer relationships and booking transactions
resource: entities
tags: [entity, dimension, sales-rep, sales-person, account-manager]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative

## Business Definition

Stores information about sales personnel responsible for managing customer relationships and booking transactions.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_sales_rep

**Source System**: QuoteToBooking

**Entity Type**: Dimension

---

## Attributes

- **Sales Representative Key** (sales_rep_key): Surrogate key that uniquely identifies a sales representative record in the sales representative dimension
- **Sales Representative ID** (rep_id): Business identifier assigned to the sales representative
- **Sales Representative Name** (rep_name): Full name of the sales representative associated with the booking
- **Sales Role** (sales_role): Job role or account responsibility of the sales representative
- **Sales Team** (sales_team): Team or organizational unit to which the sales representative belongs
- **Covered Segment** (segment_covered): Customer segment for which the sales representative is responsible

---

## Primary Keys

- **Sales Representative Key** (sales_rep_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- **[Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)**: One-to-Many relationship linking sales representatives to booking transactions

### Related Entities

- [Booking Transaction](booking-transaction.md): Fact entity that references this dimension
- [Customer](customer.md): Related through account management
- [Geography](geography.md): Related through territory coverage

---

## Measures

This dimension supports analysis of the following measures:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Concepts

- [Sales Representative](../glossary/sales-representative.md)
- [Sales Representative Key](../glossary/sales-representative-key.md)
- [Sales Representative ID](../glossary/sales-representative-id.md)
- [Sales Representative Name](../glossary/sales-representative-name.md)
- [Sales Role](../glossary/sales-role.md)
- [Sales Team](../glossary/sales-team.md)
- [Covered Segment](../glossary/covered-segment.md)

---

## Business Rules

1. Sales Representative Key is a surrogate key and must be unique
2. Sales Representative ID is the business identifier for the sales person
3. Sales Representative Name is the full name of the sales person
4. Sales Role identifies the job role or account responsibility
5. Sales Team identifies the organizational unit or team
6. Covered Segment identifies the customer segment responsibility
7. Every booking transaction must reference a valid sales representative
8. Sales representative attributes support performance and quota analysis

---

## Usage Examples

**Analysis by Sales Representative**:
- Identify top-performing sales representatives by booking revenue
- Analyze individual sales performance against quota
- Compare deal size by sales representative

**Analysis by Sales Role**:
- Compare performance across different sales roles
- Analyze role effectiveness by customer segment
- Measure role-specific productivity

**Analysis by Sales Team**:
- Evaluate team performance and contribution
- Compare team performance across geographies
- Analyze team product mix and specialization

**Analysis by Covered Segment**:
- Measure sales performance by assigned customer segment
- Analyze segment coverage effectiveness
- Compare segment specialization results

**Sales Performance Management**:
- Track individual and team quota attainment
- Analyze sales cycle and conversion metrics
- Measure average deal size by sales representative

**Territory and Account Management**:
- Evaluate account coverage by sales representative
- Analyze territory performance
- Measure customer retention by account manager

---

## Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Main Index](../index.md)
- [View Relationships](../relationships/index.md)
- [View Measures](../measures/index.md)
- [View Glossary](../glossary/index.md)
