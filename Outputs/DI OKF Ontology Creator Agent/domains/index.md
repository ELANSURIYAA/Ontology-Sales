---
title: Domains Index
type: index
description: Catalog of all business domains in the sales bookings and revenue analytics semantic model
resource: domains
tags: [domains, business, catalog, index]
timestamp: 2024-01-15T00:00:00Z
---

# Domains Index

## Overview

This catalog contains all business domains defined in the sales bookings and revenue analytics semantic model. Each domain represents a major subject area or business context.

---

## Business Domains

### [Bookings](bookings.md)
Individual completed sales booking transactions with financial measures, quantities, renewal status, and dimensional links.

**Related Entities**: Booking Transaction  
**Related Measures**: 11 measures

---

### [Customers](customers.md)
Customer organizations that place orders, including identity, segment, industry, account tier, and headquarters location.

**Related Entities**: Customer  
**Related Measures**: All revenue and volume measures

---

### [Products](products.md)
Products and offers sold to customers, including product identity, family, technology domain, offer type, and business entity.

**Related Entities**: Product  
**Related Measures**: All revenue and volume measures

---

### [Partners](partners.md)
Direct and indirect sales partners involved in fulfilling customer bookings, including partner identity, type, tier, and route to market.

**Related Entities**: Partner  
**Related Measures**: All revenue and volume measures

---

### [Geographies](geographies.md)
Geographic sales territory attributes used to analyze bookings by region, theater, and country.

**Related Entities**: Geography  
**Related Measures**: All revenue and volume measures

---

### [Sales Representatives](sales-representatives.md)
Sales persons responsible for managing customer relationships and booking transactions, including role, team, and segment coverage.

**Related Entities**: Sales Representative  
**Related Measures**: All revenue and volume measures

---

### [Contracts](contracts.md)
Commercial agreement or service coverage terms associated with bookings, including contract type, duration, renewal behavior, and support coverage level.

**Related Entities**: Contract  
**Related Measures**: All revenue and volume measures

---

### [Dates](dates.md)
Calendar and fiscal time attributes used to analyze bookings across reporting periods, years, quarters, and months.

**Related Entities**: Date  
**Related Measures**: All measures (time-based analysis)

---

## Domain Summary

| Domain | Type | Entity Count | Key Purpose |
|--------|------|--------------|-------------|
| Bookings | Fact | 1 | Transaction recording |
| Customers | Dimension | 1 | Customer analysis |
| Products | Dimension | 1 | Product analysis |
| Partners | Dimension | 1 | Channel analysis |
| Geographies | Dimension | 1 | Geographic analysis |
| Sales Representatives | Dimension | 1 | Sales performance |
| Contracts | Dimension | 1 | Contract analysis |
| Dates | Dimension | 1 | Time analysis |

---

## Navigation

- [Return to Index](../index.md)
- [View Semantic Summary](../semantic_summary.md)
- [View All Entities](../entities/index.md)
- [View All Relationships](../relationships/index.md)
- [View All Measures](../measures/index.md)
