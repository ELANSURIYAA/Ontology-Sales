---
title: Relationship Index
type: index
description: Catalog of semantic relationships in the Sales Bookings and Revenue Analytics model
resource: relationships
tags: [relationships, associations, connections, index]
timestamp: 2026-07-28T00:00:00Z
---

# Relationship Index

## Overview

This index catalogs all semantic relationships in the model. Relationships define how entities are connected and enable dimensional analysis across the star schema.

---

## Relationship Catalog

### [Contract to Booking Transaction](./contract-to-booking-transaction.md)
**Relationship ID**: REL001  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Contract](../entities/contract.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Confidence**: 1.00

### [Customer to Booking Transaction](./customer-to-booking-transaction.md)
**Relationship ID**: REL002  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Customer](../entities/customer.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Confidence**: 1.00

### [Date to Booking Transaction](./date-to-booking-transaction.md)
**Relationship ID**: REL003  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Date](../entities/date.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Confidence**: 1.00

### [Geography to Booking Transaction](./geography-to-booking-transaction.md)
**Relationship ID**: REL004  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Geography](../entities/geography.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Confidence**: 1.00

### [Partner to Booking Transaction](./partner-to-booking-transaction.md)
**Relationship ID**: REL005  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Partner](../entities/partner.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Confidence**: 1.00

### [Product to Booking Transaction](./product-to-booking-transaction.md)
**Relationship ID**: REL006  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Product](../entities/product.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Confidence**: 1.00

### [Sales Representative to Booking Transaction](./sales-representative-to-booking-transaction.md)
**Relationship ID**: REL007  
**Type**: Foreign Key  
**Cardinality**: One-to-Many  
**Source**: [Sales Representative](../entities/sales-representative.md)  
**Target**: [Booking Transaction](../entities/booking-transaction.md)  
**Confidence**: 1.00

---

## Relationship Statistics

| Metric | Count |
|--------|-------|
| Total Relationships | 7 |
| One-to-Many Relationships | 7 |
| Foreign Key Relationships | 7 |
| Average Confidence Score | 1.00 |

---

## Star Schema Pattern

All relationships follow a star schema pattern with Booking Transaction as the central fact entity:

```
        Contract ────────┐
        Customer ────────┤
        Date ────────────┤
        Geography ───────┼──→ Booking Transaction (Fact)
        Partner ─────────┤
        Product ─────────┤
        Sales Rep ───────┘
```

---

## Semantic Links

- [Main Index](../index.md)
- [Semantic Summary](../semantic_summary.md)
- [Domain Index](../domains/index.md)
- [Entity Index](../entities/index.md)
- [Measure Index](../measures/index.md)
- [Glossary Index](../glossary/index.md)

---

## Metadata

**Resource Type**: Relationship Catalog  
**Total Relationships**: 7  
**Model Pattern**: Star Schema  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
