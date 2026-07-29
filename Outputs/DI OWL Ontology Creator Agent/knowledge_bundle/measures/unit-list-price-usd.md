---
title: Unit List Price USD
type: measure
description: Standard list price per unit in U.S. dollars before discounts are applied
resource: measures
tags: [price, pricing, list-price, metric]
timestamp: 2026-07-28T00:00:00Z
---

# Unit List Price USD

## Business Definition

Standard list price per unit in U.S. dollars before discounts are applied. This measure represents the published price for products or services before any pricing adjustments or discounts.

---

## Measure Identifier

**Measure ID:** MEA002  
**Source Entity:** [Booking Transaction](../entities/booking-transaction.md)

---

## Technical Mapping

**Source Table:** QuoteToBooking.fact_bookings  
**Source Column:** unit_list_price_usd  
**Data Type:** Numeric

---

## Aggregation

**Aggregation Type:** SUM  
**Business Logic:** Sum of all unit list price values across selected transactions

---

## Business Formula

```
Total Unit List Price = SUM(unit_list_price_usd)
Average Unit List Price = AVG(unit_list_price_usd)
```

---

## Related Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Source entity for this measure
- **[Product](../entities/product.md)** - Products with list prices
- **[Customer](../entities/customer.md)** - Customers paying list prices
- **[Partner](../entities/partner.md)** - Partners selling at list prices

---

## Related Domains

- **[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)** - Primary domain

---

## Business Use Cases

1. **Pricing Strategy** - Analyze standard pricing across product portfolio
2. **Discount Analysis** - Compare list price to actual booking amount
3. **Price Positioning** - Evaluate pricing by product family and technology domain
4. **Revenue Potential** - Calculate potential revenue at list price
5. **Pricing Trends** - Track list price changes over time

---

## Analysis Dimensions

This measure can be analyzed across:

- [Product](../entities/product.md) - Product family, technology domain, offer type
- [Customer](../entities/customer.md) - Segment, industry, account tier
- [Partner](../entities/partner.md) - Partner type, partner tier
- [Geography](../entities/geography.md) - Region, theater, country
- [Date](../entities/date.md) - Fiscal year, quarter, period
- [Contract](../entities/contract.md) - Contract type, term

---

## Related Measures

- [Booking Amount USD](./booking-amount-usd.md) - Actual revenue after discounts
- [Discount Percentage](./discount-percentage.md) - Discount applied to list price
- [Quantity Sold](./quantity-sold.md) - Volume sold at list price

---

## Calculated Relationships

```
Potential Revenue = Unit List Price USD × Quantity Sold
Discount Amount = (Unit List Price USD × Quantity Sold) - Booking Amount USD
```

---

## Glossary Reference

- [Unit List Price USD](../glossary/unit-list-price-usd.md)

---

## Navigation

- [Return to Measures Index](./index.md)
- [View Metrics Summary](../metrics.md)
- [View Source Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
