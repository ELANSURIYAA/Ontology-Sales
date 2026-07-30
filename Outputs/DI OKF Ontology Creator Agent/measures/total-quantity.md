---
title: Total Quantity
type: measure
description: Total number of units, licenses, or services booked
resource: measures
tags: [quantity, volume, units, metric]
timestamp: 2024-01-15T00:00:00Z
---

# Total Quantity

## Business Definition

Total number of units, licenses, or services booked. This measure provides the aggregate quantity of items sold across all booking transactions.

---

## Measure Details

**Measure Type**: Sum  
**Aggregation**: SUM  
**Unit**: Units/Licenses  
**Category**: Volume Metric

---

## Formula

```sql
SUM(bookings.quantity)
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

- Track total units or licenses sold
- Calculate average selling price per unit
- Analyze product adoption rates
- Monitor license deployment
- Compare volume across products and time periods

---

## Business Context

Total Quantity represents the aggregate number of units, licenses, or services booked. This measure is particularly important for subscription and license-based products where quantity directly impacts revenue and customer adoption metrics.

---

## Related Measures

- [Average Selling Price USD](average-selling-price-usd.md) - Uses Total Quantity in calculation
- [Total Booking Amount USD](total-booking-amount-usd.md) - Revenue counterpart
- [Booking Count](booking-count.md) - Transaction count

---

## Related Concepts

- [Quantity](../glossary/quantity.md)
- [Unit List Price USD](../glossary/unit-list-price-usd.md)

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Summary](../metrics.md)
