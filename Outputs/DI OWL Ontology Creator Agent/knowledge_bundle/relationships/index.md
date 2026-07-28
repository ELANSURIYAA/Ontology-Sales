---
title: Relationships Index
type: index
description: Catalog of semantic relationships in the Sales Bookings and Revenue Analytics model
resource: relationships
tags: [relationships, index, foreign-keys, associations, star-schema]
timestamp: 2026-07-28T00:00:00Z
---

# Relationships Index

## Overview

This index catalogs all semantic relationships in the Sales Bookings and Revenue Analytics semantic model. All relationships follow a star schema pattern with Booking Transaction as the central fact table connected to seven dimensional entities.

---

## Relationship Catalog

### [Contract to Booking Transaction](contract-to-booking-transaction.md)
**Relationship ID**: REL001  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Contract](../entities/contract.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Description**: Links contract agreements to booking transactions

---

### [Customer to Booking Transaction](customer-to-booking-transaction.md)
**Relationship ID**: REL002  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Customer](../entities/customer.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Description**: Links customer organizations to booking transactions

---

### [Date to Booking Transaction](date-to-booking-transaction.md)
**Relationship ID**: REL003  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Date](../entities/date.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Description**: Links reporting dates to booking transactions

---

### [Geography to Booking Transaction](geography-to-booking-transaction.md)
**Relationship ID**: REL004  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Geography](../entities/geography.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Description**: Links geographic regions to booking transactions

---

### [Partner to Booking Transaction](partner-to-booking-transaction.md)
**Relationship ID**: REL005  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Partner](../entities/partner.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Description**: Links partner organizations to booking transactions

---

### [Product to Booking Transaction](product-to-booking-transaction.md)
**Relationship ID**: REL006  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Product](../entities/product.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Description**: Links products and offers to booking transactions

---

### [Sales Representative to Booking Transaction](sales-representative-to-booking-transaction.md)
**Relationship ID**: REL007  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Sales Representative](../entities/sales-representative.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Description**: Links sales personnel to booking transactions

---

## Relationship Statistics

| Metric | Count |
|--------|-------|
| Total Relationships | 7 |
| Foreign Key Relationships | 7 |
| One-to-Many Relationships | 7 |
| Dimensional Relationships | 7 |

---

## Star Schema Visualization

```
                    Contract ──────┐
                                   │
    Customer ──────┐               │
                   │               │
    Date ──────────┤               │
                   │               │
    Geography ─────┼───► Booking Transaction (FACT)
                   │               │
    Partner ───────┤               │
                   │               │
    Product ───────┘               │
                                   │
    Sales Representative ──────────┘
```

---

## Relationship Details

### Dimensional Relationships

All relationships connect dimensional entities to the central Booking Transaction fact table:

| Source Dimension | Target Fact | Foreign Key | Cardinality |
|------------------|-------------|-------------|-------------|
| Contract | Booking Transaction | contract_key | One-to-Many |
| Customer | Booking Transaction | customer_key | One-to-Many |
| Date | Booking Transaction | date_key | One-to-Many |
| Geography | Booking Transaction | geography_key | One-to-Many |
| Partner | Booking Transaction | partner_key | One-to-Many |
| Product | Booking Transaction | product_key | One-to-Many |
| Sales Representative | Booking Transaction | sales_rep_key | One-to-Many |

---

## Relationship Integrity

### Referential Integrity Rules

1. **Foreign Key Constraints**: All foreign keys in Booking Transaction must reference valid dimension records
2. **Mandatory Relationships**: Every booking transaction should link to all seven dimensions
3. **Orphan Prevention**: No booking transactions should exist without valid dimensional context
4. **Cascade Rules**: Dimension updates should maintain referential integrity with fact records

---

## Navigation

### By Source Entity
- [Contract Relationships](contract-to-booking-transaction.md)
- [Customer Relationships](customer-to-booking-transaction.md)
- [Date Relationships](date-to-booking-transaction.md)
- [Geography Relationships](geography-to-booking-transaction.md)
- [Partner Relationships](partner-to-booking-transaction.md)
- [Product Relationships](product-to-booking-transaction.md)
- [Sales Representative Relationships](sales-representative-to-booking-transaction.md)

### Related Content
- [View All Entities](../entities/index.md)
- [View All Domains](../domains/index.md)
- [View All Measures](../measures/index.md)
- [View Semantic Summary](../semantic_summary.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Total Relationships**: 7  
**Data Model Pattern**: Star Schema  
**Fact Table**: Booking Transaction  
**Dimension Count**: 7  
**Last Updated**: 2026-07-28T00:00:00Z  
**Format**: Open Knowledge Format (OKF)
