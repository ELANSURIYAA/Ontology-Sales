---
title: Distinct Order Count
type: measure
description: Count of distinct sales orders associated with booking transactions
resource: measures
tags: [order-count, volume, distinct-count, metric]
timestamp: 2024-01-15T00:00:00Z
---

# Distinct Order Count

## Business Definition

Count of distinct sales orders associated with booking transactions. This measure provides the total number of unique sales orders, as each order may contain multiple booking line items.

---

## Measure Details

**Measure Type**: Distinct Count  
**Aggregation**: COUNT DISTINCT  
**Unit**: Count  
**Category**: Volume Metric

---

## Formula

```sql
COUNT(DISTINCT bookings.order_number)
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

- Track the total number of unique sales orders
- Distinguish between order-level and line-level analysis
- Calculate average lines per order
- Analyze order complexity
- Monitor order processing volume

---

## Business Context

Distinct Order Count represents the number of unique sales orders. Since each order can have multiple line items (booking transactions), this measure will typically be lower than Booking Count. The ratio between Booking Count and Distinct Order Count indicates the average number of line items per order.

---

## Related Measures

- [Booking Count](booking-count.md) - Total transaction count including all lines
- [Total Booking Amount USD](total-booking-amount-usd.md) - Revenue by order

---

## Related Concepts

- [Order Number](../glossary/order-number.md)
- [Order Line Number](../glossary/order-line-number.md)

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Summary](../metrics.md)
