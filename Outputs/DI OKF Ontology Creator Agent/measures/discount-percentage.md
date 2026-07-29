---
title: Discount Percentage
type: measure
description: Discount applied to the list price for the booking line
resource: measures
tags: [okf, measure, discount, pricing, margin]
timestamp: 2026-07-28T00:00:00Z
---

# Discount Percentage

## Business Definition

Discount Percentage represents the discount applied to the list price for the booking line, expressed as a percentage. This measure is critical for analyzing pricing pressure, margin impact, and discount effectiveness across different dimensions.

---

## Technical Mapping

**Source Entity**: [Booking Fact](../entities/booking-fact.md)  
**Technical Column**: discount_pct  
**Data Type**: numeric(5,2)  
**Nullable**: Yes

---

## Measure Properties

**Aggregation Type**: Average  
**Measure Category**: Pricing Measure  
**Additive**: No (Semi-Additive)

---

## Formula

```
Average Discount Percentage = AVG(discount_pct)
```

The measure is typically calculated as an average across booking transactions, as discount percentages should not be summed.

---

## Related Entities

- [Booking Fact](../entities/booking-fact.md)
- [Customer Dimension](../entities/customer-dimension.md)
- [Product Dimension](../entities/product-dimension.md)
- [Partner Dimension](../entities/partner-dimension.md)

---

## Related Domains

- [Pricing](../domains/pricing.md)
- [Sales Transactions](../domains/sales-transactions.md)
- [Customer Management](../domains/customer-management.md)

---

## Business Rules

1. Discount Percentage must be between 0 and 100
2. Discount percentages are typically analyzed as averages, not sums
3. Discounts should comply with discount approval policies
4. Zero discount indicates full list price
5. Higher discounts indicate greater pricing pressure

---

## Analytical Use Cases

- Monitor average discount rates by dimension
- Analyze discount trends over time
- Compare discounts across customer segments, products, and partners
- Identify high-discount transactions requiring review
- Assess margin impact of discounting
- Support pricing optimization initiatives
- Track discount compliance with policies

---

## Related Measures

- [Unit List Price USD](unit-list-price-usd.md) - List price before discount
- [Booking Amount USD](booking-amount-usd.md) - Net revenue after discount
- [Quantity Sold](quantity-sold.md) - Volume sold with discount

---

## Calculation Examples

### Average Discount Percentage
```
AVG(discount_pct)
```

### Weighted Average Discount
```
SUM(discount_pct * booking_amount_usd) / SUM(booking_amount_usd)
```

### Discount by Customer Segment
```
AVG(discount_pct) GROUP BY customer_segment
```

### Price Realization Rate
```
(1 - AVG(discount_pct)/100) * 100
```

### Effective Price
```
unit_list_price_usd * (1 - discount_pct/100)
```

---

## Navigation

- [Back to Measures Index](index.md)
- [Back to Bundle Index](../index.md)
