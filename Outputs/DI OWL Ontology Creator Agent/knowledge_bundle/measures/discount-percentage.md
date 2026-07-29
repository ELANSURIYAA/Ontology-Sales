---
title: Discount Percentage
type: measure
description: Percentage discount applied to the list price for the booking transaction
resource: measures
tags: [discount, pricing, percentage, metric]
timestamp: 2026-07-28T00:00:00Z
---

# Discount Percentage

## Business Definition

Percentage discount applied to the list price for the booking transaction. This measure represents the pricing concession given to customers, expressed as a percentage of the list price.

---

## Measure Identifier

**Measure ID:** MEA003  
**Source Entity:** [Booking Transaction](../entities/booking-transaction.md)

---

## Technical Mapping

**Source Table:** QuoteToBooking.fact_bookings  
**Source Column:** discount_pct  
**Data Type:** Numeric

---

## Aggregation

**Aggregation Type:** AVG  
**Business Logic:** Average of discount percentages across selected transactions

---

## Business Formula

```
Average Discount Percentage = AVG(discount_pct)
Weighted Average Discount = SUM(discount_pct × booking_amount_usd) / SUM(booking_amount_usd)
```

---

## Related Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Source entity for this measure
- **[Product](../entities/product.md)** - Products with discounts
- **[Customer](../entities/customer.md)** - Customers receiving discounts
- **[Partner](../entities/partner.md)** - Partners offering discounts
- **[Contract](../entities/contract.md)** - Contracts with discount terms

---

## Related Domains

- **[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)** - Primary domain

---

## Business Use Cases

1. **Discount Analysis** - Track discount levels across transactions
2. **Margin Analysis** - Evaluate impact of discounts on profitability
3. **Pricing Strategy** - Optimize discount policies by segment and product
4. **Partner Analysis** - Compare discount patterns by partner type
5. **Customer Analysis** - Analyze discount levels by customer segment and tier

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

- [Unit List Price USD](./unit-list-price-usd.md) - Base price before discount
- [Booking Amount USD](./booking-amount-usd.md) - Revenue after discount
- [Quantity Sold](./quantity-sold.md) - Volume sold with discount

---

## Calculated Relationships

```
Booking Amount = (Unit List Price USD × Quantity Sold) × (1 - Discount Percentage)
Discount Impact = (Unit List Price USD × Quantity Sold) × Discount Percentage
```

---

## Glossary Reference

- [Discount Percentage](../glossary/discount-percentage.md)

---

## Navigation

- [Return to Measures Index](./index.md)
- [View Metrics Summary](../metrics.md)
- [View Source Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
