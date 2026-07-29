---
title: Date to Booking Relationship
type: relationship
description: Foreign key relationship linking time attributes to booking transactions
resource: relationships
tags: [okf, relationship, date, booking, foreign-key]
timestamp: 2026-07-28T00:00:00Z
---

# Date to Booking Relationship

## Business Description

This relationship links calendar and fiscal time attributes to individual booking transactions, enabling analysis of bookings across dates, months, years, quarters, and fiscal periods. Each booking transaction references a specific date through the date foreign key.

---

## Technical Mapping

**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Date Dimension](../entities/date-dimension.md)  
**Attribute**: date_key  
**Role**: Parent (One side)

---

## Target Entity

**Entity**: [Booking Fact](../entities/booking-fact.md)  
**Attribute**: date_key  
**Role**: Child (Many side)

---

## Relationship Semantics

- One date can have many booking transactions
- Each booking transaction must reference exactly one date
- The relationship enables time-based analysis of booking performance
- Date attributes provide context for understanding booking trends and seasonality

---

## Business Rules

1. Every booking must reference a valid date record
2. Date key in Booking Fact must exist in Date Dimension
3. Date attributes remain consistent for a given date key
4. Referential integrity must be maintained between dimensions and fact

---

## Analytical Use Cases

- Analyze sales performance over time
- Track revenue trends by fiscal period
- Compare year-over-year and quarter-over-quarter performance
- Monitor monthly booking patterns
- Support fiscal reporting and planning
- Enable time-based forecasting

---

## Related Concepts

### Related Domains
- [Time Management](../domains/time-management.md)
- [Sales Transactions](../domains/sales-transactions.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)

---

## Navigation

- [Back to Relationships Index](index.md)
- [Back to Bundle Index](../index.md)
