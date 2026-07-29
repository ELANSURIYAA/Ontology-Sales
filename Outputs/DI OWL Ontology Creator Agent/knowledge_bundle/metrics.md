---
title: Business Metrics
type: index
description: Complete catalog of business measures and KPIs for Sales Bookings and Revenue Analytics
resource: knowledge_bundle
tags: [metrics, measures, kpi, financial, operational]
timestamp: 2026-07-28T00:00:00Z
---

# Business Metrics

## Overview

This document catalogs all business measures and key performance indicators (KPIs) available in the Sales Bookings and Revenue Analytics domain. All measures are derived from the [Booking Transaction](./entities/booking-transaction.md) fact entity.

---

## Financial Measures

### Revenue Measures

#### [Booking Amount USD](./measures/booking-amount-usd.md)
- **Definition:** Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments
- **Aggregation:** SUM
- **Business Use:** Primary revenue metric for sales performance analysis

#### [Annual Contract Value USD](./measures/annual-contract-value-usd.md)
- **Definition:** Annualized value of the contract associated with the booking in U.S. dollars
- **Aggregation:** SUM
- **Business Use:** Subscription and recurring revenue analysis

#### [Total Contract Value USD](./measures/total-contract-value-usd.md)
- **Definition:** Total value of the full contract associated with the booking in U.S. dollars
- **Aggregation:** SUM
- **Business Use:** Long-term contract value analysis

---

## Pricing Measures

#### [Unit List Price USD](./measures/unit-list-price-usd.md)
- **Definition:** Standard list price per unit in U.S. dollars before discounts are applied
- **Aggregation:** SUM
- **Business Use:** Pricing strategy and discount analysis

#### [Discount Percentage](./measures/discount-percentage.md)
- **Definition:** Percentage discount applied to the list price for the booking transaction
- **Aggregation:** AVG
- **Business Use:** Discount effectiveness and margin analysis

---

## Operational Measures

#### [Quantity Sold](./measures/quantity-sold.md)
- **Definition:** Number of units, licenses, or subscriptions included in the booking transaction
- **Aggregation:** SUM
- **Business Use:** Volume analysis and capacity planning

---

## Measure Relationships

### Calculated Relationships

```
Booking Amount USD = (Unit List Price USD × Quantity Sold) × (1 - Discount Percentage)
```

### Measure Dependencies

- **Booking Amount USD** depends on:
  - Unit List Price USD
  - Quantity Sold
  - Discount Percentage

- **Annual Contract Value USD** relates to:
  - Total Contract Value USD
  - Contract Term Months (from [Contract](./entities/contract.md))

---

## Analysis Dimensions

All measures can be analyzed across the following dimensions:

- **[Customer](./entities/customer.md)** - Segment, industry, account tier
- **[Product](./entities/product.md)** - Product family, technology domain, offer type
- **[Partner](./entities/partner.md)** - Partner type, partner tier, route to market
- **[Geography](./entities/geography.md)** - Region, theater, country
- **[Date](./entities/date.md)** - Fiscal year, fiscal quarter, calendar year
- **[Sales Representative](./entities/sales-representative.md)** - Sales role, sales team
- **[Contract](./entities/contract.md)** - Contract type, term, coverage level

---

## Key Performance Indicators (KPIs)

### Revenue KPIs
- Total Booking Amount by Fiscal Period
- Annual Contract Value by Customer Segment
- Total Contract Value by Product Family
- Average Booking Amount per Transaction

### Operational KPIs
- Total Quantity Sold by Product
- Average Discount Percentage by Partner Type
- Booking Count by Sales Representative
- Renewal Rate (based on Booking Type)

### Efficiency KPIs
- Average Unit List Price by Product Family
- Discount Impact on Booking Amount
- Contract Value per Customer
- Booking Amount per Sales Representative

---

## Measure Catalog Summary

| Measure | Type | Aggregation | Source Entity |
|---------|------|-------------|---------------|
| [Quantity Sold](./measures/quantity-sold.md) | Operational | SUM | Booking Transaction |
| [Unit List Price USD](./measures/unit-list-price-usd.md) | Pricing | SUM | Booking Transaction |
| [Discount Percentage](./measures/discount-percentage.md) | Pricing | AVG | Booking Transaction |
| [Booking Amount USD](./measures/booking-amount-usd.md) | Financial | SUM | Booking Transaction |
| [Annual Contract Value USD](./measures/annual-contract-value-usd.md) | Financial | SUM | Booking Transaction |
| [Total Contract Value USD](./measures/total-contract-value-usd.md) | Financial | SUM | Booking Transaction |

---

## Navigation

- [Return to Bundle Index](./index.md)
- [View Semantic Summary](./semantic_summary.md)
- [View All Measures](./measures/index.md)
- [View Booking Transaction Entity](./entities/booking-transaction.md)
