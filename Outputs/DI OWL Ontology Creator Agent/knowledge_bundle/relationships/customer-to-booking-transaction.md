---
title: Customer to Booking Transaction
type: relationship
description: Foreign key relationship linking customer organizations to booking transactions
resource: relationships
tags: [relationship, foreign-key, customer, booking, one-to-many]
timestamp: 2026-07-28T00:00:00Z
---

# Customer to Booking Transaction

## Business Definition

Links customer organizations to booking transactions, enabling analysis of booking performance by customer characteristics including segment, industry, account tier, and headquarters location.

---

## Relationship Details

**Relationship ID**: REL002  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Customer](../entities/customer.md)  
**Attribute**: Customer Key (customer_key)  
**Role**: Parent/Dimension

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Customer Key (customer_key)  
**Role**: Child/Fact

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer  
**Source Column**: customer_key  
**Target Table**: QuoteToBooking.fact_bookings  
**Target Column**: customer_key  
**Join Type**: INNER JOIN

---

## Business Description

Each booking transaction is associated with exactly one customer organization that placed the order. A single customer can have multiple booking transactions over time as they purchase products and services.

This relationship enables business users to:
- Analyze booking amounts by customer segment
- Track customer lifetime value
- Evaluate industry-specific performance
- Assess account tier effectiveness
- Identify top customers by revenue
- Analyze customer concentration and diversification

---

## Relationship Rules

1. **Cardinality**: One customer can have many booking transactions (One-to-Many)
2. **Referential Integrity**: Every booking transaction must reference a valid customer record
3. **Mandatory**: Customer Key is required in booking transactions for complete analysis
4. **Immutable**: Customer association should not change after booking is recorded

---

## Usage Examples

### Analyze Bookings by Customer Segment
```sql
SELECT c.segment, SUM(b.booking_amount_usd)
FROM dim_customer c
JOIN fact_bookings b ON c.customer_key = b.customer_key
GROUP BY c.segment
```

### Identify Top Customers
```sql
SELECT c.customer_name, SUM(b.booking_amount_usd) as total_bookings
FROM dim_customer c
JOIN fact_bookings b ON c.customer_key = b.customer_key
GROUP BY c.customer_name
ORDER BY total_bookings DESC
LIMIT 10
```

---

## Related Concepts

### Related Entities
- [Customer](../entities/customer.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

### Related Glossary Terms
- [Customer](../glossary/customer.md)
- [Customer Key](../glossary/customer-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [View Relationships Index](index.md)
- [View Customer Entity](../entities/customer.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Relationship ID**: REL002  
**Source**: Customer  
**Target**: Booking Transaction  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Last Updated**: 2026-07-28T00:00:00Z
