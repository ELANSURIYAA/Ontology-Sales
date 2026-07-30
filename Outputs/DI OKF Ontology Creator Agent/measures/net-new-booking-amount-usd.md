---
title: Net New Booking Amount USD
type: measure
description: Total booked sales amount in US dollars for non-renewal transactions
resource: measures
tags: [net-new, revenue, usd, metric]
timestamp: 2024-01-15T00:00:00Z
---

# Net New Booking Amount USD

## Business Definition

Total booked sales amount in US dollars for non-renewal transactions. This measure represents revenue from new customer acquisitions and expansions.

---

## Measure Details

**Measure Type**: Conditional Sum  
**Aggregation**: SUM with CASE  
**Unit**: USD  
**Category**: Revenue Metric

---

## Formula

```sql
SUM(CASE WHEN bookings.is_renewal = 0 THEN bookings.booking_amount_usd ELSE 0 END)
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

- Track new business revenue performance
- Calculate new customer acquisition
- Analyze growth from new business
- Monitor sales pipeline effectiveness
- Compare net new vs renewal business mix

---

## Business Context

Net New Booking Amount USD represents revenue from non-renewal transactions (where is_renewal = 0), including new customer acquisitions and expansion deals with existing customers. This metric is critical for understanding business growth from new sources. Together with Renewal Booking Amount USD, it decomposes Total Booking Amount USD into renewal and new business components.

---

## Related Measures

- [Renewal Booking Amount USD](renewal-booking-amount-usd.md) - Complementary measure
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
