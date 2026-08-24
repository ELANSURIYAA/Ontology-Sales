---
title: Bookings to Customers
type: relationship
description: Links booking transactions to customer accounts
resource: relationships
tags: [bookings, customers, many-to-one, relationship]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Customers

## Business Definition

The Bookings to Customers relationship links individual booking transactions to customer accounts. This relationship enables analysis of booking performance by customer segment, industry, account tier, and headquarters location. It supports customer analytics, segmentation strategies, and account management.

---

## Relationship Type

**Many-to-one**

Multiple booking transactions can be associated with the same customer account.

---

## Source Entity

**[Bookings](../entities/bookings.md)**

The fact table containing individual completed sales booking transactions.

---

## Target Entity

**[Customers](../entities/customers.md)**

The dimension table containing customer descriptive information.

---

## Cardinality

**Many Bookings : One Customer**

- Each booking transaction references exactly one customer account
- Multiple booking transactions can be associated with the same customer
- Customer records can exist without associated bookings

---

## Join Specification

### Left Join Key
- **Field**: customer_key
- **Entity**: Bookings
- **Type**: Foreign Key

### Right Join Key
- **Field**: customer_key
- **Entity**: Customers
- **Type**: Primary Key

### Join Condition
```sql
bookings.customer_key = customers.customer_key
```

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings

**Target Table**: quotetobooking.dim_customer

**Join Column**: customer_key

---

## Business Purpose

This relationship enables:

- **Customer Segmentation**: Analyze booking performance by customer segment (Enterprise, Service Provider, Public Sector)
- **Industry Analysis**: Track booking patterns by industry vertical
- **Account Tier Analysis**: Evaluate performance by strategic account tier
- **Geographic Analysis**: Analyze bookings by customer headquarters location
- **Customer Lifetime Value**: Calculate total booking value per customer
- **Customer Retention**: Track repeat booking behavior and customer loyalty

---

## Related Measures

All booking measures can be analyzed by customer attributes:
- [Booking Count](../measures/booking-count.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

---

## Related Concepts

- [Customer Segment](../glossary/customer-segment.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Geography Region](../glossary/geography-region.md)

---

## Business Rules

1. **Mandatory Relationship**: Every booking must reference a valid customer
2. **Referential Integrity**: customer_key in bookings must exist in customers dimension
3. **One Customer per Booking**: Each booking references exactly one customer account
4. **Customer Independence**: Customers can exist without bookings (prospect accounts)

---

## Usage Examples

### Customer Segment Analysis
```sql
SELECT 
    customers.segment,
    COUNT(bookings.booking_id) as booking_count,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN customers ON bookings.customer_key = customers.customer_key
GROUP BY customers.segment
```

### Top Customers Analysis
```sql
SELECT 
    customers.customer_name,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN customers ON bookings.customer_key = customers.customer_key
GROUP BY customers.customer_name
ORDER BY total_booking_amount DESC
LIMIT 10
```

---

## Data Quality Rules

- customer_key in bookings must not be null
- customer_key in bookings must reference valid customer_key in customers
- No orphaned bookings without customer references
- Customer dimension must be populated before booking transactions

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
