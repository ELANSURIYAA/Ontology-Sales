---
title: Metrics Summary
type: index
description: Complete catalog of business measures and KPIs for sales bookings and revenue analytics
resource: knowledge_bundle
tags: [metrics, measures, kpi, sales, revenue, bookings]
timestamp: 2026-07-28T00:00:00Z
---

# Metrics Summary

## Overview

This document provides a complete catalog of all business measures and key performance indicators (KPIs) available in the sales bookings and revenue analytics semantic model.

---

## Metric Categories

### Volume Metrics
Measures tracking transaction counts and quantities

### Revenue Metrics
Measures tracking booking amounts and contract values

### Pricing Metrics
Measures tracking pricing, discounts, and average values

### Renewal Metrics
Measures tracking renewal vs. net new business

---

## Volume Metrics

### [Booking Count](./measures/booking-count.md)
**Description**: Count of booking transaction records

**Business Purpose**: Track the total number of individual booking transactions processed

**Aggregation**: COUNT

**Related Entities**: [Bookings](./entities/bookings.md)

---

### [Distinct Order Count](./measures/distinct-order-count.md)
**Description**: Count of distinct sales orders associated with booking transactions

**Business Purpose**: Track the number of unique sales orders, as each order may contain multiple booking line items

**Aggregation**: COUNT DISTINCT

**Related Entities**: [Bookings](./entities/bookings.md)

---

### [Total Quantity](./measures/total-quantity.md)
**Description**: Total number of units, licenses, or services booked

**Business Purpose**: Track the total volume of products or services sold across all bookings

**Aggregation**: SUM

**Related Entities**: [Bookings](./entities/bookings.md)

---

## Revenue Metrics

### [Total Booking Amount USD](./measures/total-booking-amount-usd.md)
**Description**: Total booked sales amount in US dollars after pricing and discount adjustments

**Business Purpose**: Primary revenue metric representing the total value of all completed bookings

**Aggregation**: SUM

**Related Entities**: [Bookings](./entities/bookings.md)

**Related Glossary**: [Booking Amount](./glossary/booking-amount.md)

---

### [Total ACV USD](./measures/total-acv-usd.md)
**Description**: Total annual contract value in US dollars

**Business Purpose**: Track the annualized revenue value of contracts for subscription and recurring revenue analysis

**Aggregation**: SUM

**Related Entities**: [Bookings](./entities/bookings.md)

**Related Glossary**: [Annual Contract Value](./glossary/annual-contract-value.md)

---

### [Total TCV USD](./measures/total-tcv-usd.md)
**Description**: Total contract value in US dollars

**Business Purpose**: Track the full contract value over the entire contract term for long-term revenue planning

**Aggregation**: SUM

**Related Entities**: [Bookings](./entities/bookings.md)

**Related Glossary**: [Total Contract Value](./glossary/total-contract-value.md)

---

## Pricing Metrics

### [Average Discount Percentage](./measures/average-discount-pct.md)
**Description**: Average discount applied to booked items or services, stored as a fractional percentage

**Business Purpose**: Monitor pricing strategy effectiveness and discount trends across bookings

**Aggregation**: AVG

**Related Entities**: [Bookings](./entities/bookings.md)

**Related Glossary**: [Discount Percentage](./glossary/discount-percentage.md)

---

### [Average Selling Price USD](./measures/average-selling-price-usd.md)
**Description**: Average booked revenue per unit sold in US dollars

**Business Purpose**: Track the effective selling price per unit after discounts and pricing adjustments

**Aggregation**: Calculated (SUM / SUM)

**Related Entities**: [Bookings](./entities/bookings.md)

---

### [Average Booking Value USD](./measures/average-booking-value-usd.md)
**Description**: Average booking value in US dollars per distinct booking transaction

**Business Purpose**: Track the average transaction size to understand deal size trends

**Aggregation**: Calculated (SUM / COUNT)

**Related Entities**: [Bookings](./entities/bookings.md)

---

## Renewal Metrics

### [Renewal Booking Amount USD](./measures/renewal-booking-amount-usd.md)
**Description**: Total booked sales amount in US dollars for renewal transactions

**Business Purpose**: Track revenue from existing customer renewals to measure customer retention and recurring revenue

**Aggregation**: Conditional SUM

**Related Entities**: [Bookings](./entities/bookings.md)

**Related Glossary**: [Renewal](./glossary/renewal.md)

---

### [Net New Booking Amount USD](./measures/net-new-booking-amount-usd.md)
**Description**: Total booked sales amount in US dollars for non-renewal transactions

**Business Purpose**: Track revenue from new business to measure customer acquisition and growth

**Aggregation**: Conditional SUM

**Related Entities**: [Bookings](./entities/bookings.md)

**Related Glossary**: [Net New Business](./glossary/net-new-business.md)

---

## Metric Relationships

### Booking Amount Decomposition
```
Total Booking Amount USD = Renewal Booking Amount USD + Net New Booking Amount USD
```

### Average Calculations
```
Average Selling Price USD = Total Booking Amount USD / Total Quantity
Average Booking Value USD = Total Booking Amount USD / Booking Count
```

---

## Dimensional Analysis

All metrics can be analyzed across the following dimensions:

- **Time**: [Dates](./entities/dates.md) - Calendar and fiscal periods
- **Customer**: [Customers](./entities/customers.md) - Segment, industry, account tier
- **Product**: [Products](./entities/products.md) - Family, technology domain, offer type
- **Partner**: [Partners](./entities/partners.md) - Type, tier, route to market
- **Geography**: [Geographies](./entities/geographies.md) - Region, theater, country
- **Sales Rep**: [Sales Representatives](./entities/sales-representatives.md) - Role, team, segment
- **Contract**: [Contracts](./entities/contracts.md) - Type, term, coverage level

---

## Usage Examples

### Revenue Analysis
- Track total booking amount by fiscal quarter
- Compare ACV vs TCV by product family
- Analyze renewal vs net new revenue trends

### Performance Analysis
- Monitor booking count by sales representative
- Track average booking value by customer segment
- Analyze order count by partner type

### Pricing Analysis
- Track average discount percentage by product family
- Monitor average selling price trends over time
- Compare pricing across geographic regions

---

## Metric Validation

✓ All metrics have valid SQL expressions  
✓ All metrics reference valid entities  
✓ All aggregations are properly defined  
✓ All calculated metrics handle division by zero  
✓ All conditional metrics have valid filters  

---

## Complete Metric Index

1. [Booking Count](./measures/booking-count.md)
2. [Distinct Order Count](./measures/distinct-order-count.md)
3. [Total Quantity](./measures/total-quantity.md)
4. [Total Booking Amount USD](./measures/total-booking-amount-usd.md)
5. [Total ACV USD](./measures/total-acv-usd.md)
6. [Total TCV USD](./measures/total-tcv-usd.md)
7. [Average Discount Percentage](./measures/average-discount-pct.md)
8. [Average Selling Price USD](./measures/average-selling-price-usd.md)
9. [Renewal Booking Amount USD](./measures/renewal-booking-amount-usd.md)
10. [Net New Booking Amount USD](./measures/net-new-booking-amount-usd.md)
11. [Average Booking Value USD](./measures/average-booking-value-usd.md)
