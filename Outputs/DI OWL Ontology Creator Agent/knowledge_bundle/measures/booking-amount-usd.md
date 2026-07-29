---
title: Booking Amount USD
type: measure
description: Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments
resource: measures
tags: [booking, revenue, financial, metric]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Amount USD

## Business Definition

Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments. This measure represents the actual revenue recognized from each booking transaction after applying discounts and pricing adjustments.

---

## Measure Identifier

**Measure ID:** MEA004  
**Source Entity:** [Booking Transaction](../entities/booking-transaction.md)

---

## Technical Mapping

**Source Table:** QuoteToBooking.fact_bookings  
**Source Column:** booking_amount_usd  
**Data Type:** Numeric

---

## Aggregation

**Aggregation Type:** SUM  
**Business Logic:** Sum of all booking amounts across selected transactions

---

## Business Formula

```
Total Booking Amount = SUM(booking_amount_usd)
Booking Amount = (Unit List Price USD × Quantity Sold) × (1 - Discount Percentage)
```

---

## Related Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Source entity for this measure
- **[Customer](../entities/customer.md)** - Customers generating revenue
- **[Product](../entities/product.md)** - Products generating revenue
- **[Partner](../entities/partner.md)** - Partners facilitating revenue
- **[Geography](../entities/geography.md)** - Geographic revenue distribution
- **[Sales Representative](../entities/sales-representative.md)** - Sales representatives generating revenue

---

## Related Domains

- **[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)** - Primary domain

---

## Business Use Cases

1. **Revenue Analysis** - Track total booked revenue across all dimensions
2. **Performance Tracking** - Measure sales performance against targets
3. **Trend Analysis** - Analyze revenue trends over time
4. **Segment Analysis** - Compare revenue contribution by customer segment
5. **Product Performance** - Evaluate revenue by product family and technology domain

---

## Analysis Dimensions

This measure can be analyzed across:

- [Customer](../entities/customer.md) - Segment, industry, account tier
- [Product](../entities/product.md) - Product family, technology domain, offer type
- [Partner](../entities/partner.md) - Partner type, partner tier, route to market
- [Geography](../entities/geography.md) - Region, theater, country
- [Date](../entities/date.md) - Fiscal year, quarter, period
- [Sales Representative](../entities/sales-representative.md) - Sales role, team, covered segment
- [Contract](../entities/contract.md) - Contract type, term, coverage level

---

## Related Measures

- [Annual Contract Value USD](./annual-contract-value-usd.md) - Annualized contract value
- [Total Contract Value USD](./total-contract-value-usd.md) - Total contract value
- [Unit List Price USD](./unit-list-price-usd.md) - List price before discount
- [Discount Percentage](./discount-percentage.md) - Discount applied
- [Quantity Sold](./quantity-sold.md) - Volume sold

---

## Key Performance Indicators

- Total Booking Amount by Fiscal Period
- Average Booking Amount per Transaction
- Booking Amount Growth Rate
- Booking Amount per Customer
- Booking Amount per Sales Representative

---

## Glossary Reference

- [Booking Amount USD](../glossary/booking-amount-usd.md)

---

## Navigation

- [Return to Measures Index](./index.md)
- [View Metrics Summary](../metrics.md)
- [View Source Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
