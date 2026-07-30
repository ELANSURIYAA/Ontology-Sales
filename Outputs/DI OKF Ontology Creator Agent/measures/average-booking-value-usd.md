---
title: Average Booking Value USD
type: measure
description: Average booking value in US dollars per distinct booking transaction
resource: measures
tags: [average-booking-value, average, usd, metric]
timestamp: 2024-01-15T00:00:00Z
---

# Average Booking Value USD

## Business Definition

Average booking value in US dollars per distinct booking transaction. This measure calculates the mean revenue value per individual booking.

---

## Measure Details

**Measure Type**: Calculated Average  
**Aggregation**: SUM / COUNT DISTINCT  
**Unit**: USD  
**Category**: Average Metric

---

## Formula

```sql
SUM(bookings.booking_amount_usd) / NULLIF(COUNT(DISTINCT bookings.booking_id), 0)
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

- Calculate average deal size
- Analyze transaction value trends
- Compare booking sizes across dimensions
- Monitor deal size evolution
- Assess sales effectiveness

---

## Business Context

Average Booking Value USD represents the mean revenue per booking transaction, calculated by dividing total booking amount by the count of distinct booking transactions. This metric provides insight into typical deal sizes and can reveal trends in customer purchasing behavior, product mix, and sales effectiveness.

---

## Related Measures

- [Total Booking Amount USD](total-booking-amount-usd.md) - Numerator
- [Booking Count](booking-count.md) - Denominator
- [Average Selling Price USD](average-selling-price-usd.md) - Per unit average

---

## Related Concepts

- [Booking Amount USD](../glossary/booking-amount-usd.md)
- [Booking ID](../glossary/booking-id.md)

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Summary](../metrics.md)
