---
title: Geography to Booking Transaction
type: relationship
description: One-to-Many relationship linking geographies to booking transactions
resource: relationships
tags: [relationship, foreign-key, geography, booking-transaction, location]
timestamp: 2026-07-28T00:00:00Z
---

# Geography to Booking Transaction

## Business Description

This relationship links geography records to booking transactions, enabling analysis of bookings by sales region, sales theater, and country.

---

## Relationship Details

**Source Entity**: [Geography](../entities/geography.md)

**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Relationship Type**: Foreign Key

**Cardinality**: One-to-Many

**Confidence Score**: 1.00

---

## Technical Mapping

**Parent Table**: QuoteToBooking.dim_geography

**Parent Column**: geography_key

**Child Table**: QuoteToBooking.fact_bookings

**Child Column**: geography_key

---

## Cardinality Explanation

- **One Geography** can be associated with **Many Booking Transactions**
- **Each Booking Transaction** must reference **exactly one Geography**

This relationship enables:
- Analysis of booking amounts by sales region
- Evaluation of theater-level performance
- Measurement of country-specific results
- Geographic market analysis

---

## Business Rules

1. Every booking transaction must reference a valid geography
2. A geography can be associated with zero or many booking transactions
3. Geography Key is the foreign key in the booking transaction fact table
4. The relationship is mandatory on the booking transaction side
5. The relationship supports referential integrity

---

## Related Concepts

- [Geography](../glossary/geography.md)
- [Geography Key](../glossary/geography-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Sales Region](../glossary/sales-region.md)
- [Sales Theater](../glossary/sales-theater.md)
- [Country](../glossary/country.md)

---

## Usage Examples

**Analyze bookings by sales region**:
- Compare regional booking performance
- Measure regional market share

**Analyze bookings by sales theater**:
- Evaluate theater-level results
- Compare theater performance within regions

**Analyze bookings by country**:
- Identify top-performing countries
- Measure country-specific adoption

**Geographic hierarchy analysis**:
- Drill down from region to theater to country
- Roll up country results to higher levels

---

## Navigation

- [Back to Relationships Index](index.md)
- [View Source Entity: Geography](../entities/geography.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Back to Main Index](../index.md)
