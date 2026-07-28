---
title: Date to Booking Transaction
type: relationship
description: Foreign key relationship linking reporting dates to booking transactions
resource: relationships
tags: [relationship, foreign-key, date, booking, one-to-many, time]
timestamp: 2026-07-28T00:00:00Z
---

# Date to Booking Transaction

## Business Definition

Links reporting dates to booking transactions, enabling time-based analysis of booking performance across calendar and fiscal periods including trending, period-over-period comparisons, and fiscal reporting.

---

## Relationship Details

**Relationship ID**: REL003  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Date](../entities/date.md)  
**Attribute**: Date Key (date_key)  
**Role**: Parent/Dimension

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Booking Date Key (date_key)  
**Role**: Child/Fact

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_date  
**Source Column**: date_key  
**Target Table**: QuoteToBooking.fact_bookings  
**Target Column**: date_key  
**Join Type**: INNER JOIN

---

## Business Description

Each booking transaction is associated with exactly one date representing when the booking was completed and recorded. A single date can have multiple booking transactions as multiple bookings may occur on the same day.

This relationship enables business users to:
- Analyze booking trends over time
- Compare fiscal period performance
- Calculate year-over-year growth
- Identify seasonal patterns
- Support fiscal and calendar reporting
- Track period-to-date metrics

---

## Relationship Rules

1. **Cardinality**: One date can have many booking transactions (One-to-Many)
2. **Referential Integrity**: Every booking transaction must reference a valid date record
3. **Mandatory**: Date Key is required in booking transactions for time-based analysis
4. **Immutable**: Booking date should not change after transaction is recorded

---

## Usage Examples

### Analyze Bookings by Fiscal Quarter
```sql
SELECT d.fiscal_quarter, SUM(b.booking_amount_usd)
FROM dim_date d
JOIN fact_bookings b ON d.date_key = b.date_key
GROUP BY d.fiscal_quarter
ORDER BY d.fiscal_period_seq
```

### Calculate Year-over-Year Growth
```sql
SELECT d.fiscal_year, SUM(b.booking_amount_usd) as annual_bookings
FROM dim_date d
JOIN fact_bookings b ON d.date_key = b.date_key
GROUP BY d.fiscal_year
ORDER BY d.fiscal_year
```

---

## Related Concepts

### Related Entities
- [Date](../entities/date.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

### Related Glossary Terms
- [Date](../glossary/date.md)
- [Date Key](../glossary/date-key.md)
- [Booking Date Key](../glossary/booking-date-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [View Relationships Index](index.md)
- [View Date Entity](../entities/date.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Relationship ID**: REL003  
**Source**: Date  
**Target**: Booking Transaction  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Last Updated**: 2026-07-28T00:00:00Z
