---
title: Average Discount Percentage
type: measure
description: Average discount applied to booked items or services, stored as a fractional percentage
resource: measures
tags: [discount, average, percentage, metric]
timestamp: 2024-01-15T00:00:00Z
---

# Average Discount Percentage

## Business Definition

Average discount applied to booked items or services, stored as a fractional percentage of list price. This measure provides insight into pricing and discount effectiveness.

---

## Measure Details

**Measure Type**: Average  
**Aggregation**: AVG  
**Unit**: Percentage (fractional)  
**Category**: Average Metric

---

## Formula

```sql
AVG(bookings.discount_pct)
```

---

## Related Entities

- [Booking Transaction](../entities/bookings.md)

---

## Related Domains

- [Bookings Domain](../domains/bookings.md)

---

## Usage

This measure is used to:

- Monitor discount levels and trends
- Analyze pricing effectiveness
- Compare discount rates across dimensions
- Identify discount patterns by customer, product, or partner
- Track margin impact

---

## Business Context

Average Discount Percentage represents the mean discount rate applied to bookings. Discounts are stored as fractional percentages (e.g., 0.15 = 15% discount). This metric helps understand pricing strategies, competitive pressure, and margin management. Higher discounts may indicate competitive markets or strategic customer investments.

---

## Related Measures

- [Total Booking Amount USD](total-booking-amount-usd.md) - Net revenue after discounts
- [Average Selling Price USD](average-selling-price-usd.md) - Realized price per unit

---

## Related Concepts

- [Discount Percentage](../glossary/discount-pct.md)
- [Unit List Price USD](../glossary/unit-list-price-usd.md)
- [Booking Amount USD](../glossary/booking-amount-usd.md)

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Summary](../metrics.md)
