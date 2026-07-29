---
title: Relationships Index
type: index
description: Complete catalog of business relationships in the Sales Bookings and Revenue Analytics knowledge bundle
resource: relationships
tags: [relationships, index, catalog, foreign-keys]
timestamp: 2026-07-28T00:00:00Z
---

# Relationships Index

## Overview

This index catalogs all business relationships in the Sales Bookings and Revenue Analytics knowledge bundle. All relationships connect dimensional entities to the central Booking Transaction fact entity through foreign key relationships.

---

## Relationship Catalog

### [Contract to Booking Transaction](./contract-to-booking-transaction.md)
**Relationship ID:** REL001  
**Type:** Foreign Key  
**Cardinality:** One-to-Many  
**Description:** Links contract records to booking transactions, enabling analysis of bookings by contract type, term, and coverage level.

---

### [Customer to Booking Transaction](./customer-to-booking-transaction.md)
**Relationship ID:** REL002  
**Type:** Foreign Key  
**Cardinality:** One-to-Many  
**Description:** Links customer records to booking transactions, enabling analysis of bookings by customer segment, industry, and account tier.

---

### [Date to Booking Transaction](./date-to-booking-transaction.md)
**Relationship ID:** REL003  
**Type:** Foreign Key  
**Cardinality:** One-to-Many  
**Description:** Links date records to booking transactions, enabling temporal analysis by fiscal year, quarter, and period.

---

### [Geography to Booking Transaction](./geography-to-booking-transaction.md)
**Relationship ID:** REL004  
**Type:** Foreign Key  
**Cardinality:** One-to-Many  
**Description:** Links geography records to booking transactions, enabling spatial analysis by region, theater, and country.

---

### [Partner to Booking Transaction](./partner-to-booking-transaction.md)
**Relationship ID:** REL005  
**Type:** Foreign Key  
**Cardinality:** One-to-Many  
**Description:** Links partner records to booking transactions, enabling analysis of bookings by partner type, tier, and route to market.

---

### [Product to Booking Transaction](./product-to-booking-transaction.md)
**Relationship ID:** REL006  
**Type:** Foreign Key  
**Cardinality:** One-to-Many  
**Description:** Links product records to booking transactions, enabling analysis of bookings by product family, technology domain, and offer type.

---

### [Sales Representative to Booking Transaction](./sales-representative-to-booking-transaction.md)
**Relationship ID:** REL007  
**Type:** Foreign Key  
**Cardinality:** One-to-Many  
**Description:** Links sales representative records to booking transactions, enabling analysis of bookings by sales role, team, and covered segment.

---

## Relationship Statistics

- **Total Relationships:** 7
- **Relationship Type:** Foreign Key
- **Cardinality Pattern:** One-to-Many
- **Source Entities:** 7 dimensional entities
- **Target Entity:** 1 fact entity (Booking Transaction)

---

## Relationship Pattern

All relationships follow a star schema pattern where dimensional entities connect to the central fact entity:

```
Contract ──────────┐
Customer ──────────┤
Date ──────────────┤
Geography ─────────┼──→ Booking Transaction
Partner ───────────┤
Product ───────────┤
Sales Representative ┘
```

---

## Navigation

- [Return to Bundle Index](../index.md)
- [View Semantic Summary](../semantic_summary.md)
- [View All Entities](../entities/index.md)
- [View All Domains](../domains/index.md)
- [View All Measures](../measures/index.md)
