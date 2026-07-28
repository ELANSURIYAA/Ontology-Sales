---
title: Partner to Booking Transaction
type: relationship
description: Foreign key relationship from Partner to Booking Transaction.
resource: relationships
tags: [relationship, partner, booking-transaction, foreign-key]
timestamp: 2026-07-28
---

# Partner to Booking Transaction

## Source Entity
- [Partner](../entities/partner.md)

## Target Entity
- [Booking Transaction](../entities/booking-transaction.md)

## Relationship Type
Foreign Key

## Cardinality
One-to-Many

## Business Description
A partner may be associated with multiple booking transactions through Partner Key, supporting channel and route-to-market performance analysis.

## Technical Mapping
- Parent Attribute: Partner Key
- Child Attribute: Partner Key
- Parent Table: `QuoteToBooking.dim_partner`
- Child Table: `QuoteToBooking.fact_bookings`

## Semantic Links
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Relationships Index](index.md)
- [Partner](../entities/partner.md)
- [Booking Transaction](../entities/booking-transaction.md)
