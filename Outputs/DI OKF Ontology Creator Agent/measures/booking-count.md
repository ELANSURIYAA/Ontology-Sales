---
title: Booking Count
type: measure
description: Count of booking transaction records
resource: measures
tags: [booking-count, volume, count, metric]
timestamp: 2024-01-15T00:00:00Z
---

# Booking Count

## Business Definition

Count of booking transaction records. This measure provides the total number of individual booking transactions in the dataset.

---

## Measure Details

**Measure Type**: Count  
**Aggregation**: COUNT  
**Unit**: Count  
**Category**: Volume Metric

---

## Formula

```sql
COUNT(bookings.booking_id)
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

- Track the total number of booking transactions
- Calculate average booking values
- Analyze transaction volume trends
- Compare booking activity across dimensions
- Monitor sales activity levels

---

## Business Context

Booking Count represents the raw transaction volume and is a key indicator of sales activity. It can be analyzed across all dimensions including time, customer, product, geography, partner, sales representative, and contract.

---

## Related Measures

- [Distinct Order Count](distinct-order-count.md) - Count of unique orders
- [Average Booking Value USD](average-booking-value-usd.md) - Uses Booking Count in calculation
- [Total Booking Amount USD](total-booking-amount-usd.md) - Revenue counterpart

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Summary](../metrics.md)
