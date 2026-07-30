---
title: Average Selling Price USD
type: measure
description: Average booked revenue per unit sold in US dollars
resource: measures
tags: [selling-price, average, unit-price, metric]
timestamp: 2024-01-15T00:00:00Z
---

# Average Selling Price USD

## Business Definition

Average booked revenue per unit sold in US dollars. This measure calculates the realized price per unit after applying discounts and pricing adjustments.

---

## Measure Details

**Measure Type**: Calculated Average  
**Aggregation**: SUM / SUM  
**Unit**: USD  
**Category**: Average Metric

---

## Formula

```sql
SUM(bookings.booking_amount_usd) / NULLIF(SUM(bookings.quantity), 0)
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

- Calculate realized price per unit
- Analyze pricing effectiveness
- Compare unit economics across products
- Monitor price realization trends
- Assess discount impact on unit pricing

---

## Business Context

Average Selling Price USD represents the actual revenue realized per unit sold, calculated by dividing total booking amount by total quantity. This metric reflects the net impact of list pricing and discounts. It is a key indicator of pricing power and unit economics, particularly important for products sold by quantity or license count.

---

## Related Measures

- [Total Booking Amount USD](total-booking-amount-usd.md) - Numerator
- [Total Quantity](total-quantity.md) - Denominator
- [Average Discount Percentage](average-discount-pct.md) - Discount impact

---

## Related Concepts

- [Unit List Price USD](../glossary/unit-list-price-usd.md)
- [Booking Amount USD](../glossary/booking-amount-usd.md)
- [Quantity](../glossary/quantity.md)
- [Discount Percentage](../glossary/discount-pct.md)

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Summary](../metrics.md)
