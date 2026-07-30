---
title: Total TCV USD
type: measure
description: Total contract value in US dollars
resource: measures
tags: [tcv, revenue, contract, metric]
timestamp: 2024-01-15T00:00:00Z
---

# Total TCV USD

## Business Definition

Total contract value in US dollars. This measure represents the full contract value over the entire term, used for multi-year deal analysis.

---

## Measure Details

**Measure Type**: Sum  
**Aggregation**: SUM  
**Unit**: USD  
**Category**: Revenue Metric

---

## Formula

```sql
SUM(bookings.tcv_usd)
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

- Track total contract value across full term
- Analyze multi-year deal performance
- Calculate total committed revenue
- Compare contract sizes
- Monitor long-term revenue commitments

---

## Business Context

Total TCV USD represents the full contract value over the entire contract term. Unlike ACV which normalizes to an annual basis, TCV captures the complete value commitment. For a 3-year contract worth $300K, the TCV would be $300K while the ACV would be $100K. This metric is important for understanding total deal size and long-term revenue commitments.

---

## Related Measures

- [Total ACV USD](total-acv-usd.md) - Annualized view
- [Total Booking Amount USD](total-booking-amount-usd.md) - Total booking value
- [Renewal Booking Amount USD](renewal-booking-amount-usd.md) - Renewal component
- [Net New Booking Amount USD](net-new-booking-amount-usd.md) - Net new component

---

## Related Concepts

- [TCV USD](../glossary/tcv-usd.md)
- [Contract Type](../glossary/contract-type.md)
- [Term Months](../glossary/term-months.md)

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Summary](../metrics.md)
