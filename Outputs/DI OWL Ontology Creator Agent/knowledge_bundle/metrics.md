---
title: Business Metrics - Sales Bookings and Revenue Analytics
type: index
description: Comprehensive catalog of business measures and KPIs for sales booking analysis
resource: knowledge_bundle
tags: [metrics, measures, kpis, financial, sales, bookings]
timestamp: 2026-07-28T00:00:00Z
---

# Business Metrics - Sales Bookings and Revenue Analytics

## Overview

This document catalogs all business measures and key performance indicators (KPIs) available in the Sales Bookings and Revenue Analytics semantic model. These measures support financial analysis, sales performance tracking, and revenue recognition across all business dimensions.

---

## Measure Categories

### Volume Metrics
- [Quantity Sold](measures/quantity-sold.md)

### Pricing Metrics
- [Unit List Price USD](measures/unit-list-price-usd.md)
- [Discount Percentage](measures/discount-percentage.md)

### Revenue Metrics
- [Booking Amount USD](measures/booking-amount-usd.md)
- [Annual Contract Value USD](measures/annual-contract-value-usd.md)
- [Total Contract Value USD](measures/total-contract-value-usd.md)

---

## Detailed Measure Catalog

### Quantity Sold

**Measure ID**: MEA001
**Type**: Volume Metric
**Aggregation**: SUM
**Source Entity**: [Booking Transaction](entities/booking-transaction.md)
**Technical Column**: quantity

**Business Definition**: Number of units, licenses, or subscriptions included in the booking transaction.

**Usage**: Track sales volume across products, customers, and time periods.

**Related Dimensions**:
- [Product](entities/product.md)
- [Customer](entities/customer.md)
- [Date](entities/date.md)

[View Full Documentation →](measures/quantity-sold.md)

---

### Unit List Price USD

**Measure ID**: MEA002
**Type**: Pricing Metric
**Aggregation**: SUM
**Source Entity**: [Booking Transaction](entities/booking-transaction.md)
**Technical Column**: unit_list_price_usd

**Business Definition**: Standard list price per unit in U.S. dollars before discounts are applied.

**Usage**: Analyze standard pricing across products and calculate discount impacts.

**Related Dimensions**:
- [Product](entities/product.md)
- [Date](entities/date.md)

[View Full Documentation →](measures/unit-list-price-usd.md)

---

### Discount Percentage

**Measure ID**: MEA003
**Type**: Pricing Metric
**Aggregation**: AVG
**Source Entity**: [Booking Transaction](entities/booking-transaction.md)
**Technical Column**: discount_pct

**Business Definition**: Percentage discount applied to the list price for the booking transaction.

**Usage**: Monitor discount levels by customer segment, partner type, and sales representative.

**Related Dimensions**:
- [Customer](entities/customer.md)
- [Partner](entities/partner.md)
- [Sales Representative](entities/sales-representative.md)

[View Full Documentation →](measures/discount-percentage.md)

---

### Booking Amount USD

**Measure ID**: MEA004
**Type**: Revenue Metric
**Aggregation**: SUM
**Source Entity**: [Booking Transaction](entities/booking-transaction.md)
**Technical Column**: booking_amount_usd

**Business Definition**: Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments.

**Usage**: Primary revenue metric for sales performance analysis and financial reporting.

**Related Dimensions**:
- [Customer](entities/customer.md)
- [Product](entities/product.md)
- [Geography](entities/geography.md)
- [Date](entities/date.md)
- [Sales Representative](entities/sales-representative.md)

[View Full Documentation →](measures/booking-amount-usd.md)

---

### Annual Contract Value USD

**Measure ID**: MEA005
**Type**: Revenue Metric
**Aggregation**: SUM
**Source Entity**: [Booking Transaction](entities/booking-transaction.md)
**Technical Column**: acv_usd

**Business Definition**: Annualized value of the contract associated with the booking in U.S. dollars.

**Usage**: Analyze recurring revenue streams and subscription performance.

**Related Dimensions**:
- [Contract](entities/contract.md)
- [Customer](entities/customer.md)
- [Product](entities/product.md)
- [Date](entities/date.md)

[View Full Documentation →](measures/annual-contract-value-usd.md)

---

### Total Contract Value USD

**Measure ID**: MEA006
**Type**: Revenue Metric
**Aggregation**: SUM
**Source Entity**: [Booking Transaction](entities/booking-transaction.md)
**Technical Column**: tcv_usd

**Business Definition**: Total value of the full contract associated with the booking in U.S. dollars.

**Usage**: Analyze total contract commitments and long-term revenue potential.

**Related Dimensions**:
- [Contract](entities/contract.md)
- [Customer](entities/customer.md)
- [Product](entities/product.md)
- [Date](entities/date.md)

[View Full Documentation →](measures/total-contract-value-usd.md)

---

## Measure Relationships

### Revenue Metric Relationships

```
Booking Amount USD = Quantity Sold × (Unit List Price USD × (1 - Discount Percentage))
Annual Contract Value USD = Total Contract Value USD / Contract Term Months × 12
```

### Aggregation Rules

| Measure | Time Aggregation | Customer Aggregation | Product Aggregation |
|---------|------------------|---------------------|---------------------|
| Quantity Sold | SUM | SUM | SUM |
| Unit List Price USD | SUM | SUM | SUM |
| Discount Percentage | AVG | AVG | AVG |
| Booking Amount USD | SUM | SUM | SUM |
| Annual Contract Value USD | SUM | SUM | SUM |
| Total Contract Value USD | SUM | SUM | SUM |

---

## Common Business Calculations

### Sales Performance Metrics

**Total Bookings by Quarter**
```
SUM(Booking Amount USD) 
GROUP BY Fiscal Quarter
```

**Average Deal Size**
```
SUM(Booking Amount USD) / COUNT(DISTINCT Booking ID)
```

**Average Discount Rate**
```
AVG(Discount Percentage)
GROUP BY Customer Segment, Partner Type
```

### Growth Metrics

**Year-over-Year Booking Growth**
```
(Current Year Booking Amount - Prior Year Booking Amount) / Prior Year Booking Amount
```

**Quarter-over-Quarter ACV Growth**
```
(Current Quarter ACV - Prior Quarter ACV) / Prior Quarter ACV
```

### Efficiency Metrics

**Revenue per Sales Representative**
```
SUM(Booking Amount USD) / COUNT(DISTINCT Sales Representative ID)
```

**Average Contract Value**
```
SUM(Total Contract Value USD) / COUNT(DISTINCT Contract Key)
```

---

## Analysis Dimensions

### Primary Analysis Dimensions

All measures can be analyzed across the following dimensions:

1. **Time**: Calendar Year, Fiscal Year, Fiscal Quarter, Month
2. **Customer**: Customer Segment, Industry, Account Tier, Headquarters Region
3. **Product**: Product Family, Technology Domain, Offer Type, Business Entity
4. **Geography**: Sales Region, Sales Theater, Country
5. **Partner**: Partner Type, Partner Tier, Route to Market
6. **Sales Team**: Sales Role, Sales Team, Covered Segment
7. **Contract**: Contract Type, Contract Term, Coverage Level

---

## Measure Usage Guidelines

### Best Practices

1. **Booking Amount USD**: Use as the primary revenue metric for sales performance reporting
2. **Annual Contract Value USD**: Use for subscription and recurring revenue analysis
3. **Total Contract Value USD**: Use for long-term revenue commitment analysis
4. **Discount Percentage**: Monitor by customer segment and partner to ensure pricing discipline
5. **Quantity Sold**: Track adoption and usage patterns across products
6. **Unit List Price USD**: Analyze pricing strategy and product positioning

### Common Pitfalls

- Do not average Booking Amount USD (always sum)
- Do not sum Discount Percentage (always average)
- Ensure proper time period alignment when comparing ACV and TCV
- Account for contract term when analyzing revenue metrics

---

## Navigation

### Explore Measures
- [View All Measures](measures/index.md)

### Related Content
- [View All Entities](entities/index.md)
- [View All Relationships](relationships/index.md)
- [View Semantic Summary](semantic_summary.md)
- [Return to Bundle Index](index.md)

---

## Metadata

**Total Measures**: 6
**Source Entity**: Booking Transaction
**Measure Categories**: Volume (1), Pricing (2), Revenue (3)
**Last Updated**: 2026-07-28T00:00:00Z
**Format**: Open Knowledge Format (OKF)
