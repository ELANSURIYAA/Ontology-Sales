---
title: Sales Representative
type: entity
description: Business entity representing sales personnel responsible for managing customer relationships and booking transactions
resource: entities
tags: [entity, dimension, sales-rep, sales-team, account-manager]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative

## Business Definition

Stores information about sales personnel responsible for managing customer relationships and booking transactions. The Sales Representative entity enables analysis of individual and team sales performance, territory coverage, and sales organization effectiveness.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_sales_rep  
**Entity Type**: Dimension  
**Entity ID**: ENT007

---

## Attributes

- **Sales Representative Key** (sales_rep_key) - integer, NOT NULL
- **Sales Representative ID** (rep_id) - character varying(20), NOT NULL
- **Sales Representative Name** (rep_name) - character varying(60), NULL
- **Sales Role** (sales_role) - character varying(40), NULL
- **Sales Team** (sales_team) - character varying(40), NULL
- **Covered Segment** (segment_covered) - character varying(30), NULL

---

## Primary Keys

- **Sales Representative Key** (sales_rep_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- [Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md) - Links sales representatives to booking transactions (One-to-Many)

---

## Measures

Sales representatives are analyzed using measures from related booking transactions:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Concepts

### Related Entities
- [Booking Transaction](booking-transaction.md) - Booking transactions managed by this sales representative
- [Customer](customer.md) - Customers managed by sales representatives
- [Geography](geography.md) - Geographic territories covered by sales representatives

### Related Glossary Terms
- [Sales Representative](../glossary/sales-representative.md)
- [Sales Representative Key](../glossary/sales-representative-key.md)
- [Sales Representative ID](../glossary/sales-representative-id.md)
- [Sales Representative Name](../glossary/sales-representative-name.md)
- [Sales Role](../glossary/sales-role.md)
- [Sales Team](../glossary/sales-team.md)
- [Covered Segment](../glossary/covered-segment.md)

### Related Domains
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Uniqueness**: Each sales representative record is uniquely identified by Sales Representative Key
2. **Business Identifier**: Sales Representative ID serves as the business identifier for the sales person
3. **Role Classification**: Sales Role describes the job role or account responsibility (e.g., Account Executive, Account Manager)
4. **Team Organization**: Sales Team identifies the organizational unit to which the sales representative belongs
5. **Segment Coverage**: Covered Segment indicates the customer segment for which the sales representative is responsible
6. **Performance Accountability**: Sales representatives are accountable for booking performance in their assigned territories and segments

---

## Usage Examples

### Individual Performance Analysis
Analyze booking amounts by sales representative to identify top performers and assess individual quota attainment.

### Team Performance Analysis
Evaluate booking performance by sales team to compare team effectiveness and resource allocation.

### Role-Based Analysis
Compare booking amounts and average deal sizes across sales roles to understand role effectiveness and specialization.

### Segment Coverage Analysis
Analyze booking performance by covered segment to assess sales coverage and territory alignment.

### Sales Productivity
Calculate revenue per sales representative and average deal size to measure sales productivity and efficiency.

---

## Data Quality Notes

- Sales Representative Key is mandatory and serves as the primary key
- Sales Representative ID is mandatory and serves as the business identifier
- Sales Representative Name should be populated for all active sales personnel
- Sales Role, Team, and Covered Segment classifications support sales organization analysis
- NULL values in descriptive attributes may indicate incomplete sales representative profiles
- Sales representative dimension should include all active sales personnel

---

## Navigation

- [View Entity Index](index.md)
- [View Related Relationships](../relationships/index.md)
- [View Related Measures](../measures/index.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Entity ID**: ENT007  
**Domain**: Sales Bookings and Revenue Analytics  
**Entity Type**: Dimension  
**Attribute Count**: 6  
**Relationship Count**: 1  
**Last Updated**: 2026-07-28T00:00:00Z
