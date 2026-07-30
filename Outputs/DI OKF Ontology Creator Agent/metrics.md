---
title: Metrics Summary
type: index
description: Complete catalog of business measures and KPIs for sales bookings and revenue analytics
resource: knowledge_bundle
tags: [metrics, measures, kpi, analytics, performance]
timestamp: 2024-01-15T00:00:00Z
---

# Metrics Summary

## Overview

This document catalogs all business measures and key performance indicators (KPIs) defined in the sales bookings and revenue analytics semantic model.

---

## Metric Categories

### Volume Metrics
Measures that quantify transaction counts and quantities

### Revenue Metrics
Measures that quantify financial performance and contract values

### Average Metrics
Measures that calculate averages and rates

---

## Volume Metrics

### Booking Count
**Count of booking transaction records**

- **Type**: Count
- **Aggregation**: COUNT
- **Grain**: Booking Transaction
- [View Details](measures/booking-count.md)

### Distinct Order Count
**Count of distinct sales orders associated with booking transactions**

- **Type**: Distinct Count
- **Aggregation**: COUNT DISTINCT
- **Grain**: Sales Order
- [View Details](measures/distinct-order-count.md)

### Total Quantity
**Total number of units, licenses, or services booked**

- **Type**: Sum
- **Aggregation**: SUM
- **Unit**: Units/Licenses
- [View Details](measures/total-quantity.md)

---

## Revenue Metrics

### Total Booking Amount USD
**Total booked sales amount in US dollars after pricing and discount adjustments**

- **Type**: Sum
- **Aggregation**: SUM
- **Currency**: USD
- [View Details](measures/total-booking-amount-usd.md)

### Total ACV USD
**Total annual contract value in US dollars**

- **Type**: Sum
- **Aggregation**: SUM
- **Currency**: USD
- [View Details](measures/total-acv-usd.md)

### Total TCV USD
**Total contract value in US dollars**

- **Type**: Sum
- **Aggregation**: SUM
- **Currency**: USD
- [View Details](measures/total-tcv-usd.md)

### Renewal Booking Amount USD
**Total booked sales amount in US dollars for renewal transactions**

- **Type**: Conditional Sum
- **Aggregation**: SUM with CASE
- **Currency**: USD
- **Filter**: is_renewal = 1
- [View Details](measures/renewal-booking-amount-usd.md)

### Net New Booking Amount USD
**Total booked sales amount in US dollars for non-renewal transactions**

- **Type**: Conditional Sum
- **Aggregation**: SUM with CASE
- **Currency**: USD
- **Filter**: is_renewal = 0
- [View Details](measures/net-new-booking-amount-usd.md)

---

## Average Metrics

### Average Discount Percentage
**Average discount applied to booked items or services**

- **Type**: Average
- **Aggregation**: AVG
- **Unit**: Percentage (fractional)
- [View Details](measures/average-discount-pct.md)

### Average Selling Price USD
**Average booked revenue per unit sold in US dollars**

- **Type**: Calculated Average
- **Aggregation**: SUM / SUM
- **Currency**: USD
- [View Details](measures/average-selling-price-usd.md)

### Average Booking Value USD
**Average booking value in US dollars per distinct booking transaction**

- **Type**: Calculated Average
- **Aggregation**: SUM / COUNT DISTINCT
- **Currency**: USD
- [View Details](measures/average-booking-value-usd.md)

---

## Metric Relationships

### Revenue Decomposition
```
Total Booking Amount USD
├── Renewal Booking Amount USD
└── Net New Booking Amount USD
```

### Unit Economics
```
Average Selling Price USD = Total Booking Amount USD / Total Quantity
Average Booking Value USD = Total Booking Amount USD / Booking Count
```

### Contract Value Analysis
```
Total ACV USD - Annualized view
Total TCV USD - Full contract term view
```

---

## Usage Guidelines

### Time-Based Analysis
Use the Date dimension to analyze metrics across:
- Calendar Year
- Fiscal Year
- Fiscal Quarter
- Fiscal Period
- Month

### Dimensional Slicing
Analyze metrics by:
- Customer Segment
- Product Family
- Geography Region
- Partner Type
- Sales Team
- Contract Type

### Renewal Analysis
Compare renewal vs net new performance:
- Renewal Booking Amount USD
- Net New Booking Amount USD
- Renewal Rate (calculated)

---

## All Measures

1. [Booking Count](measures/booking-count.md)
2. [Distinct Order Count](measures/distinct-order-count.md)
3. [Total Quantity](measures/total-quantity.md)
4. [Total Booking Amount USD](measures/total-booking-amount-usd.md)
5. [Total ACV USD](measures/total-acv-usd.md)
6. [Total TCV USD](measures/total-tcv-usd.md)
7. [Average Discount Percentage](measures/average-discount-pct.md)
8. [Average Selling Price USD](measures/average-selling-price-usd.md)
9. [Renewal Booking Amount USD](measures/renewal-booking-amount-usd.md)
10. [Net New Booking Amount USD](measures/net-new-booking-amount-usd.md)
11. [Average Booking Value USD](measures/average-booking-value-usd.md)

---

## Navigation

- [Return to Index](index.md)
- [View Semantic Summary](semantic_summary.md)
- [View All Measures](measures/index.md)
- [View All Entities](entities/index.md)
