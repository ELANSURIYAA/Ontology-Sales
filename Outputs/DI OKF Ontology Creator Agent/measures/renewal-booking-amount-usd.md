---
title: Renewal Booking Amount USD
type: measure
description: Total booked sales amount in US dollars for renewal transactions
resource: measures
tags: [renewal, revenue, usd, metric]
timestamp: 2024-01-15T00:00:00Z
---

# Renewal Booking Amount USD

## Business Definition

Total booked sales amount in US dollars for renewal transactions. This measure represents revenue from existing customer contract renewals.

---

## Measure Details

**Measure Type**: Conditional Sum  
**Aggregation**: SUM with CASE  
**Unit**: USD  
**Category**: Revenue Metric

---

## Formula

```sql
SUM(CASE WHEN bookings.is_renewal = 1 THEN bookings.booking_amount_usd ELSE 0 END)
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

- Track renewal revenue performance
- Calculate renewal rates
- Analyze customer retention
- Monitor recurring revenue health
- Compare renewal vs net new business mix

---

## Business Context

Renewal Booking Amount USD represents revenue from existing customer contract renewals (where is_renewal = 1). This metric is critical for understanding customer retention and recurring revenue health. Together with Net New Booking Amount USD, it decomposes Total Booking Amount USD into renewal and new business components.

---

## Related Measures

- [Net New Booking Amount USD](net-new-booking-amount-usd.md) - Complementary measure
- [Total Booking Amount USD](total-booking-amount-usd.md) - Total including renewals and net new
- [Total ACV USD](total-acv-usd.md) - Annualized view
- [Total TCV USD](total-tcv-usd.md) - Full contract term view

---

## Related Concepts

- [Is Renewal](../glossary/is-renewal.md)
- [Booking Type](../glossary/booking-type.md)
- [Booking Amount USD](../glossary/booking-amount-usd.md)

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Summary](../metrics.md)
