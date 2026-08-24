---
title: Bookings to Partners
type: relationship
description: Links booking transactions to sales partners
resource: relationships
tags: [bookings, partners, many-to-one, relationship, channel]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Partners

## Business Definition

The Bookings to Partners relationship links individual booking transactions to sales partners involved in fulfilling customer bookings. This relationship enables analysis of booking performance by partner type, partner tier, and route to market, supporting channel strategy optimization and partner performance management.

---

## Relationship Type

**Many-to-one**

Multiple booking transactions can be associated with the same sales partner.

---

## Source Entity

**[Bookings](../entities/bookings.md)**

The fact table containing individual completed sales booking transactions.

---

## Target Entity

**[Partners](../entities/partners.md)**

The dimension table containing sales partner information.

---

## Cardinality

**Many Bookings : One Partner**

- Each booking transaction references exactly one partner record
- Multiple booking transactions can be associated with the same partner
- Partner records can exist without associated bookings

---

## Join Specification

### Left Join Key
- **Field**: partner_key
- **Entity**: Bookings
- **Type**: Foreign Key

### Right Join Key
- **Field**: partner_key
- **Entity**: Partners
- **Type**: Primary Key

### Join Condition
```sql
bookings.partner_key = partners.partner_key
```

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings

**Target Table**: quotetobooking.dim_partner

**Join Column**: partner_key

---

## Business Purpose

This relationship enables:

- **Partner Type Analysis**: Analyze booking performance by partner type (distributor, reseller, systems integrator, direct)
- **Partner Tier Analysis**: Track performance by partner program tier
- **Route to Market Analysis**: Evaluate effectiveness of different sales channels
- **Partner Performance**: Rank partners by booking contribution
- **Channel Strategy**: Optimize channel mix and partner investments
- **Partner Development**: Identify high-performing partners for strategic relationships

---

## Related Measures

All booking measures can be analyzed by partner attributes:
- [Booking Count](../measures/booking-count.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Average Discount Percentage](../measures/average-discount-pct.md)

---

## Related Concepts

- [Partner Type](../glossary/partner-type.md)
- [Route to Market](../glossary/route-to-market.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

1. **Mandatory Relationship**: Every booking must reference a valid partner
2. **Referential Integrity**: partner_key in bookings must exist in partners dimension
3. **One Partner per Booking**: Each booking references exactly one partner record
4. **Partner Independence**: Partners can exist without bookings (registered partners)

---

## Usage Examples

### Partner Type Analysis
```sql
SELECT 
    partners.partner_type,
    COUNT(bookings.booking_id) as booking_count,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN partners ON bookings.partner_key = partners.partner_key
GROUP BY partners.partner_type
```

### Top Partners Analysis
```sql
SELECT 
    partners.partner_name,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN partners ON bookings.partner_key = partners.partner_key
GROUP BY partners.partner_name
ORDER BY total_booking_amount DESC
LIMIT 10
```

---

## Data Quality Rules

- partner_key in bookings must not be null
- partner_key in bookings must reference valid partner_key in partners
- No orphaned bookings without partner references
- Partner dimension must be populated before booking transactions

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
