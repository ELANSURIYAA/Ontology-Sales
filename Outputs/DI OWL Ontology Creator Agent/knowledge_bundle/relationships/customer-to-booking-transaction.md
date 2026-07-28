---
title: Customer to Booking Transaction
type: relationship
description: One-to-Many relationship linking customers to booking transactions
resource: relationships
tags: [relationship, foreign-key, customer, booking-transaction]
timestamp: 2026-07-28T00:00:00Z
---

# Customer to Booking Transaction

## Business Description

This relationship links customer records to booking transactions, enabling analysis of bookings by customer attributes such as segment, industry, account tier, and headquarters location.

---

## Relationship Details

**Source Entity**: [Customer](../entities/customer.md)

**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Relationship Type**: Foreign Key

**Cardinality**: One-to-Many

**Confidence Score**: 1.00

---

## Technical Mapping

**Parent Table**: QuoteToBooking.dim_customer

**Parent Column**: customer_key

**Child Table**: QuoteToBooking.fact_bookings

**Child Column**: customer_key

---

## Cardinality Explanation

- **One Customer** can be associated with **Many Booking Transactions**
- **Each Booking Transaction** must reference **exactly one Customer**

This relationship enables:
- Analysis of booking amounts by customer segment
- Evaluation of customer purchase patterns
- Measurement of customer lifetime value
- Analysis of industry-specific performance

---

## Business Rules

1. Every booking transaction must reference a valid customer
2. A customer can be associated with zero or many booking transactions
3. Customer Key is the foreign key in the booking transaction fact table
4. The relationship is mandatory on the booking transaction side
5. The relationship supports referential integrity

---

## Related Concepts

- [Customer](../glossary/customer.md)
- [Customer Key](../glossary/customer-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Customer Segment](../glossary/customer-segment.md)
- [Industry](../glossary/industry.md)
- [Account Tier](../glossary/account-tier.md)

---

## Usage Examples

**Analyze bookings by customer segment**:
- Compare Enterprise vs. Service Provider vs. Public Sector bookings
- Measure segment contribution to revenue

**Analyze bookings by industry**:
- Identify top-performing industries
- Evaluate industry-specific product adoption

**Analyze bookings by account tier**:
- Compare strategic vs. standard account performance
- Measure account tier revenue contribution

**Analyze customer purchase patterns**:
- Evaluate repeat purchase behavior
- Measure customer lifetime value
- Analyze cross-sell and upsell opportunities

---

## Navigation

- [Back to Relationships Index](index.md)
- [View Source Entity: Customer](../entities/customer.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
