---
title: Total Booking Amount USD
type: measure
description: Total booked sales amount in US dollars after pricing and discount adjustments
resource: measures
tags: [booking-amount, revenue, usd, metric]
timestamp: 2024-01-15T00:00:00Z
---

# Total Booking Amount USD

## Business Definition

Total booked sales amount in US dollars after pricing and discount adjustments. This measure represents the primary revenue metric for sales performance analysis.

---

## Measure Details

**Measure Type**: Sum  
**Aggregation**: SUM  
**Unit**: USD  
**Category**: Revenue Metric

---

## Formula

```sql
SUM(bookings.booking_amount_usd)
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

- Track total sales revenue
- Analyze revenue performance across dimensions
- Calculate revenue growth rates
- Monitor sales targets and quotas
- Compare performance across time periods

---

## Business Context

Total Booking Amount USD is the primary revenue metric representing the total value of completed sales bookings after applying discounts and pricing adjustments. It is calculated as: (quantity × unit_list_price_usd) × (1 - discount_pct). This measure can be decomposed into Renewal Booking Amount USD and Net New Booking Amount USD.

---

## Related Measures

- [Renewal Booking Amount USD](renewal-booking-amount-usd.md) - Renewal component
- [Net New Booking Amount USD](net-new-booking-amount-usd.md) - Net new component
- [Total ACV USD](total-acv-usd.md) - Annualized view
- [Total TCV USD](total-tcv-usd.md) - Full contract term view
- [Average Booking Value USD](average-booking-value-usd.md) - Per transaction average
- [Average Selling Price USD](average-selling-price-usd.md) - Per unit average

---

## Related Concepts

- [Booking Amount USD](../glossary/booking-amount-usd.md)
- [Unit List Price USD](../glossary/unit-list-price-usd.md)
- [Discount Percentage](../glossary/discount-pct.md)

---

## Navigation

- [Return to Measures Index](index.md)
- [Return to Main Index](../index.md)
- [View Metrics Summary](../metrics.md)
