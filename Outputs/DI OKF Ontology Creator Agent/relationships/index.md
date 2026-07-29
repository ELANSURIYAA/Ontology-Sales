---
title: Relationships Index
type: index
description: Navigation index for all entity relationships in the Quote to Booking semantic model
resource: relationships
tags: [okf, relationships, index, quote-to-booking]
timestamp: 2026-07-28T00:00:00Z
---

# Relationships Index

## Overview

This index provides navigation to all entity relationships within the Quote to Booking semantic model. The model implements a star schema pattern with 7 foreign key relationships connecting dimension entities to the central Booking Fact.

---

## Relationship Catalog

### [Contract to Booking](contract-to-booking.md)
**Relationship ID**: REL001  
**Parent Entity**: Contract Dimension  
**Child Entity**: Booking Fact  
**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Description**: Links contract attributes to booking transactions

---

### [Customer to Booking](customer-to-booking.md)
**Relationship ID**: REL002  
**Parent Entity**: Customer Dimension  
**Child Entity**: Booking Fact  
**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Description**: Links customer attributes to booking transactions

---

### [Date to Booking](date-to-booking.md)
**Relationship ID**: REL003  
**Parent Entity**: Date Dimension  
**Child Entity**: Booking Fact  
**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Description**: Links time attributes to booking transactions

---

### [Geography to Booking](geography-to-booking.md)
**Relationship ID**: REL004  
**Parent Entity**: Geography Dimension  
**Child Entity**: Booking Fact  
**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Description**: Links geographic attributes to booking transactions

---

### [Partner to Booking](partner-to-booking.md)
**Relationship ID**: REL005  
**Parent Entity**: Partner Dimension  
**Child Entity**: Booking Fact  
**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Description**: Links partner attributes to booking transactions

---

### [Product to Booking](product-to-booking.md)
**Relationship ID**: REL006  
**Parent Entity**: Product Dimension  
**Child Entity**: Booking Fact  
**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Description**: Links product attributes to booking transactions

---

### [Sales Representative to Booking](sales-representative-to-booking.md)
**Relationship ID**: REL007  
**Parent Entity**: Sales Representative Dimension  
**Child Entity**: Booking Fact  
**Relationship Type**: Foreign Key Relationship  
**Cardinality**: One-to-Many  
**Description**: Links sales representative attributes to booking transactions

---

## Relationship Statistics

- **Total Relationships**: 7
- **Foreign Key Relationships**: 7
- **One-to-Many Relationships**: 7
- **Star Schema Pattern**: Yes

---

## Star Schema Visualization

```
Contract Dimension ──────┐
                         │
Customer Dimension ──────┤
                         │
Date Dimension ──────────┤
                         │
Geography Dimension ─────┤──→ Booking Fact
                         │
Partner Dimension ───────┤
                         │
Product Dimension ───────┤
                         │
Sales Rep Dimension ─────┘
```

---

## Relationship Patterns

### Dimensional Relationships
All relationships follow the same pattern:
- **Direction**: Dimension → Fact
- **Cardinality**: One-to-Many
- **Type**: Foreign Key
- **Purpose**: Enable dimensional analysis of booking transactions

---

## Navigation

- [Back to Bundle Index](../index.md)
- [Semantic Summary](../semantic_summary.md)
- [Domains Index](../domains/index.md)
- [Entities Index](../entities/index.md)
- [Measures Index](../measures/index.md)
- [Glossary Index](../glossary/index.md)
