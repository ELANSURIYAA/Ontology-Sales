---
title: Measure Index
type: index
description: Catalog of business measures in the Sales Bookings and Revenue Analytics model
resource: measures
tags: [measures, metrics, kpi, index]
timestamp: 2026-07-28T00:00:00Z
---

# Measure Index

## Overview

This index catalogs all business measures in the semantic model. Measures represent quantifiable metrics used for sales performance analysis and revenue tracking.

---

## Measure Catalog

### Volume Measures

#### [Quantity Sold](./quantity-sold.md)
**Measure ID**: MEA001  
**Description**: Number of units, licenses, or subscriptions included in the booking transaction  
**Aggregation**: SUM  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)

---

### Pricing Measures

#### [Unit List Price USD](./unit-list-price-usd.md)
**Measure ID**: MEA002  
**Description**: Standard list price per unit in U.S. dollars before discounts are applied  
**Aggregation**: SUM  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)

#### [Discount Percentage](./discount-percentage.md)
**Measure ID**: MEA003  
**Description**: Percentage discount applied to the list price for the booking transaction  
**Aggregation**: AVG  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)

---

### Revenue Measures

#### [Booking Amount USD](./booking-amount-usd.md)
**Measure ID**: MEA004  
**Description**: Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments  
**Aggregation**: SUM  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)

#### [Annual Contract Value USD](./annual-contract-value-usd.md)
**Measure ID**: MEA005  
**Description**: Annualized value of the contract associated with the booking in U.S. dollars  
**Aggregation**: SUM  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)

#### [Total Contract Value USD](./total-contract-value-usd.md)
**Measure ID**: MEA006  
**Description**: Total value of the full contract associated with the booking in U.S. dollars  
**Aggregation**: SUM  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)

---

## Measure Statistics

| Metric | Count |
|--------|-------|
| Total Measures | 6 |
| Volume Measures | 1 |
| Pricing Measures | 2 |
| Revenue Measures | 3 |
| SUM Aggregations | 5 |
| AVG Aggregations | 1 |

---

## Measure Categories

### By Type
- **Volume**: Quantity Sold
- **Pricing**: Unit List Price USD, Discount Percentage
- **Revenue**: Booking Amount USD, Annual Contract Value USD, Total Contract Value USD

### By Aggregation
- **SUM**: Quantity Sold, Unit List Price USD, Booking Amount USD, Annual Contract Value USD, Total Contract Value USD
- **AVG**: Discount Percentage

---

## Semantic Links

- [Main Index](../index.md)
- [Metrics Overview](../metrics.md)
- [Semantic Summary](../semantic_summary.md)
- [Entity Index](../entities/index.md)
- [Booking Transaction Entity](../entities/booking-transaction.md)

---

## Metadata

**Resource Type**: Measure Catalog  
**Total Measures**: 6  
**Source Entity**: Booking Transaction  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
