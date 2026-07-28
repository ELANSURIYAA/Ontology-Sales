---
title: Measures Index
type: index
description: Catalog of business measures and metrics in the Sales Bookings and Revenue Analytics model
resource: measures
tags: [measures, index, metrics, kpis, financial]
timestamp: 2026-07-28T00:00:00Z
---

# Measures Index

## Overview

This index catalogs all business measures and key performance indicators (KPIs) in the Sales Bookings and Revenue Analytics semantic model. All measures are derived from the Booking Transaction fact table and support comprehensive financial and operational analysis.

---

## Measure Catalog

### Volume Measures

#### [Quantity Sold](quantity-sold.md)
**Measure ID**: MEA001  
**Aggregation**: SUM  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Technical Column**: quantity  
**Description**: Number of units, licenses, or subscriptions included in the booking transaction

---

### Pricing Measures

#### [Unit List Price USD](unit-list-price-usd.md)
**Measure ID**: MEA002  
**Aggregation**: SUM  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Technical Column**: unit_list_price_usd  
**Description**: Standard list price per unit in U.S. dollars before discounts are applied

#### [Discount Percentage](discount-percentage.md)
**Measure ID**: MEA003  
**Aggregation**: AVG  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Technical Column**: discount_pct  
**Description**: Percentage discount applied to the list price for the booking transaction

---

### Revenue Measures

#### [Booking Amount USD](booking-amount-usd.md)
**Measure ID**: MEA004  
**Aggregation**: SUM  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Technical Column**: booking_amount_usd  
**Description**: Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments

#### [Annual Contract Value USD](annual-contract-value-usd.md)
**Measure ID**: MEA005  
**Aggregation**: SUM  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Technical Column**: acv_usd  
**Description**: Annualized value of the contract associated with the booking in U.S. dollars

#### [Total Contract Value USD](total-contract-value-usd.md)
**Measure ID**: MEA006  
**Aggregation**: SUM  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Technical Column**: tcv_usd  
**Description**: Total value of the full contract associated with the booking in U.S. dollars

---

## Measure Statistics

| Category | Count |
|----------|-------|
| Total Measures | 6 |
| Volume Measures | 1 |
| Pricing Measures | 2 |
| Revenue Measures | 3 |

---

## Measure Summary Table

| Measure | Type | Aggregation | Unit | Source Column |
|---------|------|-------------|------|---------------|
| Quantity Sold | Volume | SUM | Units | quantity |
| Unit List Price USD | Pricing | SUM | USD | unit_list_price_usd |
| Discount Percentage | Pricing | AVG | Percent | discount_pct |
| Booking Amount USD | Revenue | SUM | USD | booking_amount_usd |
| Annual Contract Value USD | Revenue | SUM | USD | acv_usd |
| Total Contract Value USD | Revenue | SUM | USD | tcv_usd |

---

## Analysis Dimensions

All measures can be analyzed across the following dimensions:

- **Time**: [Date](../entities/date.md) - Calendar and fiscal periods
- **Customer**: [Customer](../entities/customer.md) - Segment, industry, account tier
- **Product**: [Product](../entities/product.md) - Family, technology domain, offer type
- **Geography**: [Geography](../entities/geography.md) - Region, theater, country
- **Partner**: [Partner](../entities/partner.md) - Type, tier, route to market
- **Sales Team**: [Sales Representative](../entities/sales-representative.md) - Role, team, segment
- **Contract**: [Contract](../entities/contract.md) - Type, term, coverage level

---

## Navigation

### By Category
- [Volume Measures](#volume-measures)
- [Pricing Measures](#pricing-measures)
- [Revenue Measures](#revenue-measures)

### Related Content
- [View All Entities](../entities/index.md)
- [View All Relationships](../relationships/index.md)
- [View All Domains](../domains/index.md)
- [View Metrics Overview](../metrics.md)
- [View Semantic Summary](../semantic_summary.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Total Measures**: 6  
**Source Entity**: Booking Transaction  
**Measure Categories**: Volume (1), Pricing (2), Revenue (3)  
**Last Updated**: 2026-07-28T00:00:00Z  
**Format**: Open Knowledge Format (OKF)
