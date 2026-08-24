---
title: Measures Index
type: index
description: Index of all business measures in the sales bookings and revenue analytics semantic model
resource: measures
tags: [measures, metrics, kpi, index]
timestamp: 2026-07-28T00:00:00Z
---

# Business Measures Index

## Overview

This index provides access to all business measures and key performance indicators (KPIs) defined in the sales bookings and revenue analytics semantic model. Measures are organized by category for easy navigation.

---

## Measure Categories

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

### [Booking Count](./booking-count.md)
**Description**: Count of booking transaction records

**Aggregation**: COUNT

**Expression**: COUNT(bookings.booking_id)

---

### [Distinct Order Count](./distinct-order-count.md)
**Description**: Count of distinct sales orders associated with booking transactions

**Aggregation**: COUNT DISTINCT

**Expression**: COUNT(DISTINCT bookings.order_number)

---

### [Total Quantity](./total-quantity.md)
**Description**: Total number of units, licenses, or services booked

**Aggregation**: SUM

**Expression**: SUM(bookings.quantity)

---

## Revenue Metrics

### [Total Booking Amount USD](./total-booking-amount-usd.md)
**Description**: Total booked sales amount in US dollars after pricing and discount adjustments

**Aggregation**: SUM

**Expression**: SUM(bookings.booking_amount_usd)

---

### [Total ACV USD](./total-acv-usd.md)
**Description**: Total annual contract value in US dollars

**Aggregation**: SUM

**Expression**: SUM(bookings.acv_usd)

---

### [Total TCV USD](./total-tcv-usd.md)
**Description**: Total contract value in US dollars

**Aggregation**: SUM

**Expression**: SUM(bookings.tcv_usd)

---

## Pricing Metrics

### [Average Discount Percentage](./average-discount-pct.md)
**Description**: Average discount applied to booked items or services, stored as a fractional percentage

**Aggregation**: AVG

**Expression**: AVG(bookings.discount_pct)

---

### [Average Selling Price USD](./average-selling-price-usd.md)
**Description**: Average booked revenue per unit sold in US dollars

**Aggregation**: Calculated

**Expression**: SUM(bookings.booking_amount_usd) / NULLIF(SUM(bookings.quantity), 0)

---

### [Average Booking Value USD](./average-booking-value-usd.md)
**Description**: Average booking value in US dollars per distinct booking transaction

**Aggregation**: Calculated

**Expression**: SUM(bookings.booking_amount_usd) / NULLIF(COUNT(DISTINCT bookings.booking_id), 0)

---

## Renewal Metrics

### [Renewal Booking Amount USD](./renewal-booking-amount-usd.md)
**Description**: Total booked sales amount in US dollars for renewal transactions

**Aggregation**: Conditional SUM

**Expression**: SUM(CASE WHEN bookings.is_renewal = 1 THEN bookings.booking_amount_usd ELSE 0 END)

---

### [Net New Booking Amount USD](./net-new-booking-amount-usd.md)
**Description**: Total booked sales amount in US dollars for non-renewal transactions

**Aggregation**: Conditional SUM

**Expression**: SUM(CASE WHEN bookings.is_renewal = 0 THEN bookings.booking_amount_usd ELSE 0 END)

---

## Measure Count

**Total Measures**: 11
- **Volume Metrics**: 3
- **Revenue Metrics**: 3
- **Pricing Metrics**: 3
- **Renewal Metrics**: 2

---

## Related Entities

All measures are calculated from the [Bookings](../entities/bookings.md) fact table and can be analyzed across all dimension entities:
- [Customers](../entities/customers.md)
- [Products](../entities/products.md)
- [Partners](../entities/partners.md)
- [Geographies](../entities/geographies.md)
- [Sales Representatives](../entities/sales-representatives.md)
- [Contracts](../entities/contracts.md)
- [Dates](../entities/dates.md)

---

## Navigation

- [Back to Knowledge Bundle Index](../index.md)
- [Metrics Summary](../metrics.md)
- [Semantic Summary](../semantic_summary.md)
- [Domains Index](../domains/index.md)
- [Entities Index](../entities/index.md)
- [Relationships Index](../relationships/index.md)
- [Glossary Index](../glossary/index.md)
