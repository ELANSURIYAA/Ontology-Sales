---
title: Metrics Catalog
type: index
description: Complete catalog of business metrics and measures for sales bookings and revenue analytics
resource: knowledge_bundle
tags: [metrics, measures, catalog, kpi]
timestamp: 2026-07-28T00:00:00Z
---

# Metrics Catalog

## Overview

This catalog contains all business metrics and measures defined in the sales bookings and revenue analytics semantic model.

---

## Volume Metrics

### [Booking Count](measures/booking-count.md)
Count of booking transaction records.

**Expression**: `COUNT(bookings.booking_id)`

**Related Entities**: [Bookings](entities/bookings.md)

---

### [Distinct Order Count](measures/distinct-order-count.md)
Count of distinct sales orders associated with booking transactions.

**Expression**: `COUNT(DISTINCT bookings.order_number)`

**Related Entities**: [Bookings](entities/bookings.md)

---

### [Total Quantity](measures/total-quantity.md)
Total number of units, licenses, or services booked.

**Expression**: `SUM(bookings.quantity)`

**Related Entities**: [Bookings](entities/bookings.md)

---

## Revenue Metrics

### [Total Booking Amount USD](measures/total-booking-amount-usd.md)
Total booked sales amount in US dollars after pricing and discount adjustments.

**Expression**: `SUM(bookings.booking_amount_usd)`

**Related Entities**: [Bookings](entities/bookings.md)

---

### [Total ACV USD](measures/total-acv-usd.md)
Total annual contract value in US dollars.

**Expression**: `SUM(bookings.acv_usd)`

**Related Entities**: [Bookings](entities/bookings.md)

**Related Concepts**: [Annual Contract Value](glossary/annual-contract-value.md)

---

### [Total TCV USD](measures/total-tcv-usd.md)
Total contract value in US dollars.

**Expression**: `SUM(bookings.tcv_usd)`

**Related Entities**: [Bookings](entities/bookings.md)

**Related Concepts**: [Total Contract Value](glossary/total-contract-value.md)

---

## Pricing Metrics

### [Average Discount Pct](measures/average-discount-pct.md)
Average discount applied to booked items or services, stored as a fractional percentage.

**Expression**: `AVG(bookings.discount_pct)`

**Related Entities**: [Bookings](entities/bookings.md)

---

### [Average Selling Price USD](measures/average-selling-price-usd.md)
Average booked revenue per unit sold in US dollars.

**Expression**: `SUM(bookings.booking_amount_usd) / NULLIF(SUM(bookings.quantity), 0)`

**Related Entities**: [Bookings](entities/bookings.md)

---

### [Average Booking Value USD](measures/average-booking-value-usd.md)
Average booking value in US dollars per distinct booking transaction.

**Expression**: `SUM(bookings.booking_amount_usd) / NULLIF(COUNT(DISTINCT bookings.booking_id), 0)`

**Related Entities**: [Bookings](entities/bookings.md)

---

## Business Type Metrics

### [Renewal Booking Amount USD](measures/renewal-booking-amount-usd.md)
Total booked sales amount in US dollars for renewal transactions.

**Expression**: `SUM(CASE WHEN bookings.is_renewal = 1 THEN bookings.booking_amount_usd ELSE 0 END)`

**Related Entities**: [Bookings](entities/bookings.md)

**Related Concepts**: [Renewal](glossary/renewal.md)

---

### [Net New Booking Amount USD](measures/net-new-booking-amount-usd.md)
Total booked sales amount in US dollars for non-renewal transactions.

**Expression**: `SUM(CASE WHEN bookings.is_renewal = 0 THEN bookings.booking_amount_usd ELSE 0 END)`

**Related Entities**: [Bookings](entities/bookings.md)

**Related Concepts**: [Net New Business](glossary/net-new-business.md)

---

## Metrics by Category

### Volume Analysis
- [Booking Count](measures/booking-count.md)
- [Distinct Order Count](measures/distinct-order-count.md)
- [Total Quantity](measures/total-quantity.md)

### Revenue Analysis
- [Total Booking Amount USD](measures/total-booking-amount-usd.md)
- [Total ACV USD](measures/total-acv-usd.md)
- [Total TCV USD](measures/total-tcv-usd.md)
- [Renewal Booking Amount USD](measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](measures/net-new-booking-amount-usd.md)

### Pricing Analysis
- [Average Discount Pct](measures/average-discount-pct.md)
- [Average Selling Price USD](measures/average-selling-price-usd.md)
- [Average Booking Value USD](measures/average-booking-value-usd.md)

---

## Navigation

- [Return to Index](index.md)
- [View Semantic Summary](semantic_summary.md)
- [Browse All Measures](measures/index.md)
- [Browse Entities](entities/index.md)
- [Browse Glossary](glossary/index.md)
