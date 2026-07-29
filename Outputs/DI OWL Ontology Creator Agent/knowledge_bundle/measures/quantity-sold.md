---
title: Quantity Sold
type: measure
description: Number of units, licenses, or subscriptions included in the booking transaction
resource: measures
tags: [quantity, volume, operational, metric]
timestamp: 2026-07-28T00:00:00Z
---

# Quantity Sold

## Business Definition

Number of units, licenses, or subscriptions included in the booking transaction. This measure represents the volume of products or services sold in each transaction.

---

## Measure Identifier

**Measure ID:** MEA001  
**Source Entity:** [Booking Transaction](../entities/booking-transaction.md)

---

## Technical Mapping

**Source Table:** QuoteToBooking.fact_bookings  
**Source Column:** quantity  
**Data Type:** Integer

---

## Aggregation

**Aggregation Type:** SUM  
**Business Logic:** Sum of all quantity values across selected transactions

---

## Business Formula

```
Total Quantity Sold = SUM(quantity)
```

---

## Related Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Source entity for this measure
- **[Product](../entities/product.md)** - Products being sold
- **[Customer](../entities/customer.md)** - Customers purchasing quantities
- **[Partner](../entities/partner.md)** - Partners facilitating sales

---

## Related Domains

- **[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)** - Primary domain

---

## Business Use Cases

1. **Volume Analysis** - Track total units, licenses, or subscriptions sold
2. **Product Demand** - Analyze quantity sold by product family or SKU
3. **Capacity Planning** - Forecast future demand based on historical quantities
4. **Customer Analysis** - Evaluate purchase volume by customer segment
5. **Partner Performance** - Measure volume contribution by partner

---

## Analysis Dimensions

This measure can be analyzed across:

- [Customer](../entities/customer.md) - Segment, industry, account tier
- [Product](../entities/product.md) - Product family, technology domain, offer type
- [Partner](../entities/partner.md) - Partner type, partner tier
- [Geography](../entities/geography.md) - Region, theater, country
- [Date](../entities/date.md) - Fiscal year, quarter, period
- [Sales Representative](../entities/sales-representative.md) - Sales role, team
- [Contract](../entities/contract.md) - Contract type, term

---

## Related Measures

- [Booking Amount USD](./booking-amount-usd.md) - Revenue generated from quantities sold
- [Unit List Price USD](./unit-list-price-usd.md) - Price per unit sold
- [Discount Percentage](./discount-percentage.md) - Discount applied to quantities

---

## Glossary Reference

- [Quantity Sold](../glossary/quantity-sold.md)

---

## Navigation

- [Return to Measures Index](./index.md)
- [View Metrics Summary](../metrics.md)
- [View Source Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
