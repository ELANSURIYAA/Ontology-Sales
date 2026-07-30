---
title: Measures Index
type: index
description: Catalog of all business measures in the sales bookings and revenue analytics semantic model
resource: measures
tags: [measures, metrics, kpi, index]
timestamp: 2024-01-15T00:00:00Z
---

# Measures Index

## Overview

This catalog contains all business measures defined in the sales bookings and revenue analytics semantic model. Measures are organized into volume metrics, revenue metrics, and average metrics.

---

## Volume Metrics

### [Booking Count](booking-count.md)
Count of booking transaction records.

**Aggregation**: COUNT  
**Expression**: COUNT(bookings.booking_id)

---

### [Distinct Order Count](distinct-order-count.md)
Count of distinct sales orders associated with booking transactions.

**Aggregation**: COUNT DISTINCT  
**Expression**: COUNT(DISTINCT bookings.order_number)

---

### [Total Quantity](total-quantity.md)
Total number of units, licenses, or services booked.

**Aggregation**: SUM  
**Expression**: SUM(bookings.quantity)

---

## Revenue Metrics

### [Total Booking Amount USD](total-booking-amount-usd.md)
Total booked sales amount in US dollars after pricing and discount adjustments.

**Aggregation**: SUM  
**Expression**: SUM(bookings.booking_amount_usd)

---

### [Total ACV USD](total-acv-usd.md)
Total annual contract value in US dollars.

**Aggregation**: SUM  
**Expression**: SUM(bookings.acv_usd)

---

### [Total TCV USD](total-tcv-usd.md)
Total contract value in US dollars.

**Aggregation**: SUM  
**Expression**: SUM(bookings.tcv_usd)

---

### [Renewal Booking Amount USD](renewal-booking-amount-usd.md)
Total booked sales amount in US dollars for renewal transactions.

**Aggregation**: SUM with CASE  
**Expression**: SUM(CASE WHEN bookings.is_renewal = 1 THEN bookings.booking_amount_usd ELSE 0 END)

---

### [Net New Booking Amount USD](net-new-booking-amount-usd.md)
Total booked sales amount in US dollars for non-renewal transactions.

**Aggregation**: SUM with CASE  
**Expression**: SUM(CASE WHEN bookings.is_renewal = 0 THEN bookings.booking_amount_usd ELSE 0 END)

---

## Average Metrics

### [Average Discount Percentage](average-discount-pct.md)
Average discount applied to booked items or services, stored as a fractional percentage.

**Aggregation**: AVG  
**Expression**: AVG(bookings.discount_pct)

---

### [Average Selling Price USD](average-selling-price-usd.md)
Average booked revenue per unit sold in US dollars.

**Aggregation**: Calculated  
**Expression**: SUM(bookings.booking_amount_usd) / NULLIF(SUM(bookings.quantity), 0)

---

### [Average Booking Value USD](average-booking-value-usd.md)
Average booking value in US dollars per distinct booking transaction.

**Aggregation**: Calculated  
**Expression**: SUM(bookings.booking_amount_usd) / NULLIF(COUNT(DISTINCT bookings.booking_id), 0)

---

## Measure Summary

| Measure | Category | Aggregation | Unit |
|---------|----------|-------------|------|
| Booking Count | Volume | COUNT | Count |
| Distinct Order Count | Volume | COUNT DISTINCT | Count |
| Total Quantity | Volume | SUM | Units |
| Total Booking Amount USD | Revenue | SUM | USD |
| Total ACV USD | Revenue | SUM | USD |
| Total TCV USD | Revenue | SUM | USD |
| Renewal Booking Amount USD | Revenue | SUM with CASE | USD |
| Net New Booking Amount USD | Revenue | SUM with CASE | USD |
| Average Discount Percentage | Average | AVG | Percentage |
| Average Selling Price USD | Average | Calculated | USD |
| Average Booking Value USD | Average | Calculated | USD |

---

## Navigation

- [Return to Index](../index.md)
- [View Metrics Summary](../metrics.md)
- [View Semantic Summary](../semantic_summary.md)
- [View All Entities](../entities/index.md)
