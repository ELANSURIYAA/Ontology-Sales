---
title: Sales Representative
type: entity
description: Sales personnel responsible for managing customer relationships and booking transactions
resource: entities
tags: [sales, representative, personnel, dimension, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative

## Business Definition

The Sales Representative entity stores information about sales personnel responsible for managing customer relationships and booking transactions. It captures sales representative characteristics including sales role, sales team assignment, and covered customer segment. This entity enables sales performance analysis, quota tracking, and territory management.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_sales_rep  
**Source Schema**: QuoteToBooking  
**Entity Type**: Dimension  
**Entity ID**: ENT007

---

## Attributes

- **Sales Representative Key** - Surrogate key that uniquely identifies a sales representative record in the sales representative dimension
- **Sales Representative ID** - Business identifier assigned to the sales representative
- **Sales Representative Name** - Full name of the sales representative associated with the booking
- **Sales Role** - Job role or account responsibility of the sales representative
- **Sales Team** - Team or organizational unit to which the sales representative belongs
- **Covered Segment** - Customer segment for which the sales representative is responsible

---

## Primary Keys

- **Sales Representative Key** (sales_rep_key) - Surrogate key, Integer, Not Nullable

---

## Foreign Keys

None - This is a dimension entity

---

## Relationships

### Outgoing Relationships

- **[Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)** - One-to-Many relationship linking sales representatives to booking transactions

### Related Entities

- **[Booking Transaction](./booking-transaction.md)** - Fact entity containing booking records managed by sales representatives
- **[Customer](./customer.md)** - Customers managed by sales representatives
- **[Geography](./geography.md)** - Territories covered by sales representatives
- **[Product](./product.md)** - Products sold by sales representatives

---

## Measures

Sales Representatives support performance analysis of all measures:

- **[Booking Amount USD](../measures/booking-amount-usd.md)** - Revenue by sales representative and team
- **[Annual Contract Value USD](../measures/annual-contract-value-usd.md)** - ACV by sales role
- **[Total Contract Value USD](../measures/total-contract-value-usd.md)** - TCV by sales team
- **[Quantity Sold](../measures/quantity-sold.md)** - Volume by representative
- **[Discount Percentage](../measures/discount-percentage.md)** - Pricing by sales role
- **[Unit List Price USD](../measures/unit-list-price-usd.md)** - Deal size by representative

---

## Business Rules

1. Sales Representative Key must be unique and not null
2. Sales Representative ID must be unique and not null
3. Sales Representative Name is required for all records
4. Sales Role must be from approved list (Account Executive, Account Manager, Territory Manager, etc.)
5. Sales Team must be from approved organizational structure
6. Covered Segment must align with customer segment classifications
7. Each sales representative must belong to exactly one sales team
8. Each sales representative must have exactly one primary sales role

---

## Analytical Usage

### Sales Representative Performance
- Track individual sales representative booking performance
- Compare representative productivity and effectiveness
- Analyze top performers and performance distribution

### Sales Role Analysis
- Compare booking performance across different sales roles
- Analyze role-specific contribution and specialization
- Track role effectiveness and efficiency

### Sales Team Analysis
- Evaluate team-level booking performance
- Compare team productivity and results
- Track team composition and structure

### Segment Coverage Analysis
- Analyze representative performance by covered segment
- Track segment specialization and focus
- Evaluate segment coverage effectiveness

---

## Sales Organization Hierarchy

```
Sales Team
  └─ Sales Role
      └─ Covered Segment
          └─ Sales Representative Name
```

### Example Organization

```
Enterprise Sales Team
  ├─ Account Executive
  │   ├─ Enterprise Segment
  │   │   ├─ John Smith
  │   │   └─ Jane Doe
  │   └─ Public Sector Segment
  │       └─ Bob Johnson
  └─ Account Manager
      └─ Enterprise Segment
          └─ Alice Williams

Commercial Sales Team
  ├─ Territory Manager
  │   └─ Commercial Segment
  │       ├─ Tom Brown
  │       └─ Sarah Davis
  └─ Inside Sales Representative
      └─ Small Business Segment
          └─ Mike Wilson

Service Provider Sales Team
  └─ Strategic Account Executive
      └─ Service Provider Segment
          ├─ David Lee
          └─ Emily Chen
```

---

## Related Concepts

- **[Customer](./customer.md)** - Customers managed by sales representatives
- **[Geography](./geography.md)** - Sales territories and coverage areas
- **[Product](./product.md)** - Products sold by representatives
- **[Partner](./partner.md)** - Partners supported by sales representatives
- **[Booking Transaction](./booking-transaction.md)** - Transactions credited to representatives

---

## Glossary Terms

- [Sales Representative](../glossary/sales-representative.md)
- [Sales Representative Key](../glossary/sales-representative-key.md)
- [Sales Representative ID](../glossary/sales-representative-id.md)
- [Sales Representative Name](../glossary/sales-representative-name.md)
- [Sales Role](../glossary/sales-role.md)
- [Sales Team](../glossary/sales-team.md)
- [Covered Segment](../glossary/covered-segment.md)

---

## Attribute Details

| Attribute | Technical Column | Data Type | Nullable | Key Type | Description |
|-----------|-----------------|-----------|----------|----------|-------------|
| Sales Representative Key | sales_rep_key | integer | No | Primary | Surrogate key uniquely identifying sales representative |
| Sales Representative ID | rep_id | character varying(20) | No | Business | Business identifier for sales representative |
| Sales Representative Name | rep_name | character varying(60) | Yes | - | Full name of sales representative |
| Sales Role | sales_role | character varying(40) | Yes | - | Job role or account responsibility |
| Sales Team | sales_team | character varying(40) | Yes | - | Team or organizational unit |
| Covered Segment | segment_covered | character varying(30) | Yes | - | Customer segment responsibility |

---

## Semantic Links

- [Entity Index](./index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Relationship Index](../relationships/index.md)
- [Measure Index](../measures/index.md)
- [Main Index](../index.md)

---

## Metadata

**Entity ID**: ENT007  
**Domain ID**: DOM001  
**Entity Type**: Dimension  
**Technical Table**: QuoteToBooking.dim_sales_rep  
**Total Attributes**: 6  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
