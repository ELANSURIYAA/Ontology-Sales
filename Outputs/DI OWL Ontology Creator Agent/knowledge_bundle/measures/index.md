---
title: Measures Index
type: index
description: Complete catalog of business measures in the Sales Bookings and Revenue Analytics knowledge bundle
resource: measures
tags: [measures, index, catalog, metrics, kpi]
timestamp: 2026-07-28T00:00:00Z
---

# Measures Index

## Overview

This index catalogs all business measures in the Sales Bookings and Revenue Analytics knowledge bundle. All measures are derived from the [Booking Transaction](../entities/booking-transaction.md) fact entity.

---

## Measure Catalog

### Financial Measures

#### [Booking Amount USD](./booking-amount-usd.md)
**Measure ID:** MEA004  
**Aggregation:** SUM  
**Description:** Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments.

#### [Annual Contract Value USD](./annual-contract-value-usd.md)
**Measure ID:** MEA005  
**Aggregation:** SUM  
**Description:** Annualized value of the contract associated with the booking in U.S. dollars.

#### [Total Contract Value USD](./total-contract-value-usd.md)
**Measure ID:** MEA006  
**Aggregation:** SUM  
**Description:** Total value of the full contract associated with the booking in U.S. dollars.

---

### Pricing Measures

#### [Unit List Price USD](./unit-list-price-usd.md)
**Measure ID:** MEA002  
**Aggregation:** SUM  
**Description:** Standard list price per unit in U.S. dollars before discounts are applied.

#### [Discount Percentage](./discount-percentage.md)
**Measure ID:** MEA003  
**Aggregation:** AVG  
**Description:** Percentage discount applied to the list price for the booking transaction.

---

### Operational Measures

#### [Quantity Sold](./quantity-sold.md)
**Measure ID:** MEA001  
**Aggregation:** SUM  
**Description:** Number of units, licenses, or subscriptions included in the booking transaction.

---

## Measure Statistics

- **Total Measures:** 6
- **Financial Measures:** 3
- **Pricing Measures:** 2
- **Operational Measures:** 1
- **Source Entity:** Booking Transaction

---

## Measure Categories

### Revenue Metrics
- Booking Amount USD
- Annual Contract Value USD
- Total Contract Value USD

### Pricing Metrics
- Unit List Price USD
- Discount Percentage

### Volume Metrics
- Quantity Sold

---

## Navigation

- [Return to Bundle Index](../index.md)
- [View Metrics Summary](../metrics.md)
- [View Semantic Summary](../semantic_summary.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
