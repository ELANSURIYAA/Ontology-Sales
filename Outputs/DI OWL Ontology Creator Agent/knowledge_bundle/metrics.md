---
title: Business Metrics - Sales Bookings and Revenue Analytics
type: metrics
description: Business measures and KPIs for Sales Bookings and Revenue Analytics
resource: knowledge_bundle
tags: [metrics, measures, kpi, sales, bookings, revenue]
timestamp: 2026-07-28T00:00:00Z
---

# Business Metrics - Sales Bookings and Revenue Analytics

This document provides a comprehensive overview of all business measures and KPIs available in the Sales Bookings and Revenue Analytics domain.

---

## Core Revenue Metrics

### [Booking Amount USD](measures/booking-amount-usd.md)

**Definition**: Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments.

**Aggregation**: SUM

**Entity**: [Booking Transaction](entities/booking-transaction.md)

**Technical Column**: booking_amount_usd

**Business Use**: Primary revenue metric for analyzing sales performance across all dimensions.

---

### [Annual Contract Value USD](measures/annual-contract-value-usd.md)

**Definition**: Annualized value of the contract associated with the booking in U.S. dollars.

**Aggregation**: SUM

**Entity**: [Booking Transaction](entities/booking-transaction.md)

**Technical Column**: acv_usd

**Business Use**: Measures recurring revenue potential on an annual basis.

---

### [Total Contract Value USD](measures/total-contract-value-usd.md)

**Definition**: Total value of the full contract associated with the booking in U.S. dollars.

**Aggregation**: SUM

**Entity**: [Booking Transaction](entities/booking-transaction.md)

**Technical Column**: tcv_usd

**Business Use**: Measures total contract commitment over the full contract term.

---

## Volume Metrics

### [Quantity Sold](measures/quantity-sold.md)

**Definition**: Number of units, licenses, or subscriptions included in the booking transaction.

**Aggregation**: SUM

**Entity**: [Booking Transaction](entities/booking-transaction.md)

**Technical Column**: quantity

**Business Use**: Tracks volume of products, licenses, or subscriptions sold.

---

## Pricing Metrics

### [Unit List Price USD](measures/unit-list-price-usd.md)

**Definition**: Standard list price per unit in U.S. dollars before discounts are applied.

**Aggregation**: SUM

**Entity**: [Booking Transaction](entities/booking-transaction.md)

**Technical Column**: unit_list_price_usd

**Business Use**: Baseline pricing metric for discount and margin analysis.

---

### [Discount Percentage](measures/discount-percentage.md)

**Definition**: Percentage discount applied to the list price for the booking transaction.

**Aggregation**: AVG

**Entity**: [Booking Transaction](entities/booking-transaction.md)

**Technical Column**: discount_pct

**Business Use**: Measures pricing concessions and discount trends.

---

## Measure Analysis Dimensions

All measures can be analyzed across the following dimensions:

- **[Customer](entities/customer.md)**: Customer Segment, Industry, Account Tier, Headquarters Country, Headquarters Region
- **[Product](entities/product.md)**: Product Family, Technology Domain, Offer Type, Business Entity
- **[Partner](entities/partner.md)**: Partner Type, Partner Tier, Route to Market
- **[Geography](entities/geography.md)**: Sales Region, Sales Theater, Country
- **[Sales Representative](entities/sales-representative.md)**: Sales Role, Sales Team, Covered Segment
- **[Contract](entities/contract.md)**: Contract Type, Contract Term Months, Coverage Level
- **[Date](entities/date.md)**: Fiscal Year, Fiscal Quarter, Calendar Year, Month Name

---

## Calculated Metrics

The following derived metrics can be calculated from base measures:

### Average Deal Size
**Formula**: SUM(Booking Amount USD) / COUNT(Booking ID)

### Average Discount Rate
**Formula**: AVG(Discount Percentage)

### Average Contract Term
**Formula**: AVG(Contract Term Months)

### Renewal Rate
**Formula**: SUM(Booking Amount USD WHERE Renewal Indicator = 1) / SUM(Booking Amount USD)

### Average Unit Price
**Formula**: SUM(Booking Amount USD) / SUM(Quantity Sold)

---

## Metric Relationships

```
Booking Amount USD = (Unit List Price USD × Quantity Sold) × (1 - Discount Percentage)

Total Contract Value USD = Annual Contract Value USD × (Contract Term Months / 12)
```

---

## Measure Summary Table

| Measure | Aggregation | Data Type | Entity | Technical Column |
|---------|-------------|-----------|--------|------------------|
| Quantity Sold | SUM | Integer | Booking Transaction | quantity |
| Unit List Price USD | SUM | Numeric | Booking Transaction | unit_list_price_usd |
| Discount Percentage | AVG | Numeric | Booking Transaction | discount_pct |
| Booking Amount USD | SUM | Numeric | Booking Transaction | booking_amount_usd |
| Annual Contract Value USD | SUM | Numeric | Booking Transaction | acv_usd |
| Total Contract Value USD | SUM | Numeric | Booking Transaction | tcv_usd |

---

## Business Questions Answered

These metrics enable analysis of:

- What is total booking revenue by customer segment?
- What is the average deal size by product family?
- What is the discount rate by partner type?
- What is the renewal rate by fiscal quarter?
- What is ACV by sales region?
- What is TCV by contract type?
- What is quantity sold by technology domain?
- What is average unit price by offer type?

---

## Navigation

- [Back to Index](index.md)
- [Semantic Summary](semantic_summary.md)
- [View All Measures](measures/index.md)
- [View Entities](entities/index.md)
- [View Relationships](relationships/index.md)
- [View Glossary](glossary/index.md)
