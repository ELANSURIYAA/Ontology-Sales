---
title: Geography to Booking Transaction
type: relationship
description: Foreign key relationship linking geographic regions to booking transactions
resource: relationships
tags: [relationship, foreign-key, geography, booking, one-to-many, location]
timestamp: 2026-07-28T00:00:00Z
---

# Geography to Booking Transaction

## Business Definition

Links geographic regions to booking transactions, enabling regional sales analysis by sales region, theater, and country to support market coverage evaluation and geographic performance tracking.

---

## Relationship Details

**Relationship ID**: REL004  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Geography](../entities/geography.md)  
**Attribute**: Geography Key (geography_key)  
**Role**: Parent/Dimension

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Geography Key (geography_key)  
**Role**: Child/Fact

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_geography  
**Source Column**: geography_key  
**Target Table**: QuoteToBooking.fact_bookings  
**Target Column**: geography_key  
**Join Type**: INNER JOIN

---

## Business Description

Each booking transaction is associated with exactly one geographic location representing the sales region, theater, and country where the booking occurred. A single geography can have multiple booking transactions as multiple bookings may occur in the same location.

This relationship enables business users to:
- Analyze booking amounts by sales region
- Compare theater-level performance
- Evaluate country-specific results
- Assess geographic concentration
- Identify market expansion opportunities
- Track regional sales effectiveness

---

## Relationship Rules

1. **Cardinality**: One geography can have many booking transactions (One-to-Many)
2. **Referential Integrity**: Every booking transaction must reference a valid geography record
3. **Mandatory**: Geography Key is required in booking transactions for regional analysis
4. **Immutable**: Geography association should not change after booking is recorded

---

## Usage Examples

### Analyze Bookings by Sales Region
```sql
SELECT g.region, SUM(b.booking_amount_usd)
FROM dim_geography g
JOIN fact_bookings b ON g.geography_key = b.geography_key
GROUP BY g.region
```

### Compare Theater Performance
```sql
SELECT g.theater, SUM(b.booking_amount_usd), COUNT(b.booking_id)
FROM dim_geography g
JOIN fact_bookings b ON g.geography_key = b.geography_key
GROUP BY g.theater
ORDER BY SUM(b.booking_amount_usd) DESC
```

---

## Related Concepts

### Related Entities
- [Geography](../entities/geography.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

### Related Glossary Terms
- [Geography](../glossary/geography.md)
- [Geography Key](../glossary/geography-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [View Relationships Index](index.md)
- [View Geography Entity](../entities/geography.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Relationship ID**: REL004  
**Source**: Geography  
**Target**: Booking Transaction  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Last Updated**: 2026-07-28T00:00:00Z
