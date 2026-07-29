---
title: Customer to Booking Transaction
type: relationship
description: Foreign key relationship linking customers to booking transactions
resource: relationships
tags: [customer, booking, foreign-key, one-to-many]
timestamp: 2026-07-28T00:00:00Z
---

# Customer to Booking Transaction

## Relationship Definition

Links customer records to booking transactions, enabling analysis of bookings by customer segment, industry, account tier, and headquarters location. This relationship allows business users to understand customer purchasing behavior and revenue contribution.

---

## Relationship Identifier

**Relationship ID:** REL002

---

## Source Entity

**[Customer](../entities/customer.md)**  
**Entity ID:** ENT002  
**Technical Table:** QuoteToBooking.dim_customer

---

## Target Entity

**[Booking Transaction](../entities/booking-transaction.md)**  
**Entity ID:** ENT008  
**Technical Table:** QuoteToBooking.fact_bookings

---

## Relationship Type

**Type:** Foreign Key  
**Cardinality:** One-to-Many  
**Confidence Score:** 1.00

---

## Technical Mapping

**Parent Attribute:** Customer Key (customer_key)  
**Child Attribute:** Customer Key (customer_key)  
**Join Condition:** dim_customer.customer_key = fact_bookings.customer_key

---

## Business Description

Each customer can have multiple booking transactions, but each booking transaction is associated with exactly one customer. This relationship enables analysis of:

- Booking performance by customer segment
- Revenue contribution by industry vertical
- Account tier profitability analysis
- Geographic customer distribution
- Customer lifetime value analysis

---

## Related Measures

This relationship enables customer-based analysis of:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)

---

## Business Use Cases

1. **Customer Segment Analysis** - Compare booking performance across Enterprise, Service Provider, and Public Sector segments
2. **Industry Vertical Analysis** - Analyze revenue patterns by customer industry
3. **Account Tier Analysis** - Evaluate booking performance by strategic account tier
4. **Geographic Analysis** - Track customer bookings by headquarters location
5. **Customer Profitability** - Calculate total revenue and contract value per customer

---

## Navigation

- [Return to Relationships Index](./index.md)
- [View Source Entity: Customer](../entities/customer.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
