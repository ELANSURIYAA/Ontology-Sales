---
title: Relationships Index
type: index
description: Navigation index for entity relationships
resource: relationships
tags: [relationships, index, foreign-key, cardinality]
timestamp: 2026-07-28T00:00:00Z
---

# Relationships Index

This index provides navigation to all entity relationship documents in the knowledge bundle.

---

## Relationship Overview

The knowledge bundle contains **7** entity relationships, all following a **One-to-Many** cardinality pattern from dimension entities to the fact entity.

---

## Relationship List

### [Contract to Booking Transaction](contract-to-booking-transaction.md)

**Source Entity**: [Contract](../entities/contract.md)  
**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Cardinality**: One-to-Many  
**Type**: Foreign Key  
**Description**: Links contract records to booking transactions

---

### [Customer to Booking Transaction](customer-to-booking-transaction.md)

**Source Entity**: [Customer](../entities/customer.md)  
**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Cardinality**: One-to-Many  
**Type**: Foreign Key  
**Description**: Links customer records to booking transactions

---

### [Date to Booking Transaction](date-to-booking-transaction.md)

**Source Entity**: [Date](../entities/date.md)  
**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Cardinality**: One-to-Many  
**Type**: Foreign Key  
**Description**: Links date records to booking transactions

---

### [Geography to Booking Transaction](geography-to-booking-transaction.md)

**Source Entity**: [Geography](../entities/geography.md)  
**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Cardinality**: One-to-Many  
**Type**: Foreign Key  
**Description**: Links geography records to booking transactions

---

### [Partner to Booking Transaction](partner-to-booking-transaction.md)

**Source Entity**: [Partner](../entities/partner.md)  
**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Cardinality**: One-to-Many  
**Type**: Foreign Key  
**Description**: Links partner records to booking transactions

---

### [Product to Booking Transaction](product-to-booking-transaction.md)

**Source Entity**: [Product](../entities/product.md)  
**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Cardinality**: One-to-Many  
**Type**: Foreign Key  
**Description**: Links product records to booking transactions

---

### [Sales Representative to Booking Transaction](sales-representative-to-booking-transaction.md)

**Source Entity**: [Sales Representative](../entities/sales-representative.md)  
**Target Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Cardinality**: One-to-Many  
**Type**: Foreign Key  
**Description**: Links sales representative records to booking transactions

---

## Relationship Pattern

All relationships follow a star schema pattern where:

- **Dimension entities** (Contract, Customer, Date, Geography, Partner, Product, Sales Representative) have a **One-to-Many** relationship with the **Fact entity** (Booking Transaction)
- Each booking transaction references exactly one record from each dimension
- Each dimension record can be referenced by zero or many booking transactions
- All relationships are implemented through foreign key constraints

---

## Semantic Model Structure

```
Contract ──────────┐
Customer ──────────┤
Date ──────────────┤
Geography ─────────┤──→ Booking Transaction (Fact)
Partner ───────────┤
Product ───────────┤
Sales Representative ┘
```

---

## Navigation

- [Back to Index](../index.md)
- [Semantic Summary](../semantic_summary.md)
- [View Domains](../domains/index.md)
- [View Entities](../entities/index.md)
- [View Measures](../measures/index.md)
- [View Glossary](../glossary/index.md)
