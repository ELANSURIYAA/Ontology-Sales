---
title: Date to Booking Transaction
type: relationship
description: Foreign key relationship linking dates to booking transactions
resource: relationships
tags: [date, booking, foreign-key, one-to-many, temporal]
timestamp: 2026-07-28T00:00:00Z
---

# Date to Booking Transaction

## Relationship Definition

Links date records to booking transactions, enabling temporal analysis by fiscal year, fiscal quarter, calendar year, and fiscal period. This relationship allows business users to track sales performance over time and identify trends.

---

## Relationship Identifier

**Relationship ID:** REL003

---

## Source Entity

**[Date](../entities/date.md)**  
**Entity ID:** ENT003  
**Technical Table:** QuoteToBooking.dim_date

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

**Parent Attribute:** Date Key (date_key)  
**Child Attribute:** Booking Date Key (date_key)  
**Join Condition:** dim_date.date_key = fact_bookings.date_key

---

## Business Description

Each date can be associated with multiple booking transactions, but each booking transaction occurs on exactly one date. This relationship enables analysis of:

- Booking performance by fiscal year
- Quarterly trend analysis
- Seasonal booking patterns
- Year-over-year growth comparison
- Period-over-period performance tracking

---

## Related Measures

This relationship enables time-based analysis of:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Business Use Cases

1. **Fiscal Year Analysis** - Track annual booking performance against targets
2. **Quarterly Trends** - Analyze booking patterns by fiscal quarter
3. **Seasonal Analysis** - Identify seasonal booking trends and patterns
4. **Growth Analysis** - Calculate year-over-year and quarter-over-quarter growth
5. **Period Comparison** - Compare booking performance across fiscal periods

---

## Navigation

- [Return to Relationships Index](./index.md)
- [View Source Entity: Date](../entities/date.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
