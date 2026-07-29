---
title: Geography to Booking Transaction
type: relationship
description: Foreign key relationship linking geographies to booking transactions
resource: relationships
tags: [geography, booking, foreign-key, one-to-many, spatial]
timestamp: 2026-07-28T00:00:00Z
---

# Geography to Booking Transaction

## Relationship Definition

Links geography records to booking transactions, enabling spatial analysis by sales region, theater, and country. This relationship allows business users to understand geographic sales performance and market penetration.

---

## Relationship Identifier

**Relationship ID:** REL004

---

## Source Entity

**[Geography](../entities/geography.md)**  
**Entity ID:** ENT004  
**Technical Table:** QuoteToBooking.dim_geography

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

**Parent Attribute:** Geography Key (geography_key)  
**Child Attribute:** Geography Key (geography_key)  
**Join Condition:** dim_geography.geography_key = fact_bookings.geography_key

---

## Business Description

Each geography can be associated with multiple booking transactions, but each booking transaction occurs in exactly one geography. This relationship enables analysis of:

- Booking performance by sales region
- Theater-level revenue analysis
- Country-specific booking trends
- Geographic market penetration
- Regional sales territory performance

---

## Related Measures

This relationship enables geography-based analysis of:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)

---

## Business Use Cases

1. **Regional Performance** - Compare booking performance across sales regions
2. **Theater Analysis** - Analyze revenue contribution by sales theater
3. **Country Analysis** - Track booking trends by country
4. **Market Penetration** - Evaluate geographic coverage and market share
5. **Territory Optimization** - Identify high-performing and underperforming territories

---

## Navigation

- [Return to Relationships Index](./index.md)
- [View Source Entity: Geography](../entities/geography.md)
- [View Target Entity: Booking Transaction](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
