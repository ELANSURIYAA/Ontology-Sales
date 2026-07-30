---
title: Total ACV USD
type: measure
description: Total annual contract value in US dollars
resource: measures
tags: [acv, revenue, annual, metric]
timestamp: 2024-01-15T00:00:00Z
---

# Total ACV USD

## Business Definition

Total annual contract value in US dollars. This measure represents the annualized value of bookings, used for subscription and recurring revenue analysis.

---

## Measure Details

**Measure Type**: Sum  
**Aggregation**: SUM  
**Unit**: USD  
**Category**: Revenue Metric

---

## Formula

```sql
SUM(bookings.acv_usd)
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

- Track annualized recurring revenue
- Analyze subscription business performance
- Calculate annual run rate
- Compare multi-year deals on an annual basis
- Monitor subscription growth trends

---

## Business Context

Total ACV USD represents the annualized contract value of bookings. For multi-year contracts, ACV normalizes the revenue to an annual basis, enabling consistent comparison across contracts with different term lengths. This is a critical metric for subscription and recurring revenue business models.

---

## Related Measures

- [Total TCV USD](total-tcv-usd.md) - Full contract term value
- [Total Booking Amount USD](total-booking-amount-usd.md) - Total booking value
- [Renewal Booking Amount USD](renewal-booking-amount-usd.md) - Renewal component
- [Net New Booking Amount USD](net-new-booking-amount-usd.md) - Net new component

---

## Related Concepts

- [ACV USD](../glossary/acv-usd.md)
- [Contract Type](../glossary/contract-type.md)
- [Term Months](../glossary/term-months.md)

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Summary](../metrics.md)
