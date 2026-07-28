---
title: Partner to Booking Transaction
type: relationship
description: Foreign key relationship linking partner organizations to booking transactions
resource: relationships
tags: [relationship, foreign-key, partner, booking, one-to-many, channel]
timestamp: 2026-07-28T00:00:00Z
---

# Partner to Booking Transaction

## Business Definition

Links partner organizations to booking transactions, enabling analysis of partner ecosystem performance by partner type, partner tier, and route to market to support channel effectiveness evaluation and partner strategy optimization.

---

## Relationship Details

**Relationship ID**: REL005  
**Relationship Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Confidence Score**: 1.00

---

## Source Entity

**Entity**: [Partner](../entities/partner.md)  
**Attribute**: Partner Key (partner_key)  
**Role**: Parent/Dimension

---

## Target Entity

**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Attribute**: Partner Key (partner_key)  
**Role**: Child/Fact

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_partner  
**Source Column**: partner_key  
**Target Table**: QuoteToBooking.fact_bookings  
**Target Column**: partner_key  
**Join Type**: INNER JOIN

---

## Business Description

Each booking transaction is associated with exactly one partner organization involved in the sales process. A single partner can have multiple booking transactions as they facilitate sales across multiple customers and products.

This relationship enables business users to:
- Analyze booking amounts by partner
- Compare partner type effectiveness
- Evaluate partner tier performance
- Assess route to market strategies
- Identify top-performing partners
- Monitor partner discount levels

---

## Relationship Rules

1. **Cardinality**: One partner can have many booking transactions (One-to-Many)
2. **Referential Integrity**: Every booking transaction must reference a valid partner record
3. **Mandatory**: Partner Key is required in booking transactions for channel analysis
4. **Immutable**: Partner association should not change after booking is recorded

---

## Usage Examples

### Analyze Bookings by Partner Type
```sql
SELECT p.partner_type, SUM(b.booking_amount_usd)
FROM dim_partner p
JOIN fact_bookings b ON p.partner_key = b.partner_key
GROUP BY p.partner_type
```

### Identify Top Partners
```sql
SELECT p.partner_name, SUM(b.booking_amount_usd) as total_bookings
FROM dim_partner p
JOIN fact_bookings b ON p.partner_key = b.partner_key
GROUP BY p.partner_name
ORDER BY total_bookings DESC
LIMIT 10
```

---

## Related Concepts

### Related Entities
- [Partner](../entities/partner.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

### Related Glossary Terms
- [Partner](../glossary/partner.md)
- [Partner Key](../glossary/partner-key.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [View Relationships Index](index.md)
- [View Partner Entity](../entities/partner.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Relationship ID**: REL005  
**Source**: Partner  
**Target**: Booking Transaction  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Last Updated**: 2026-07-28T00:00:00Z
