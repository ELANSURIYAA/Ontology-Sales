---
title: Unit List Price USD
type: measure
description: Standard list price per unit in U.S. dollars before discounts
resource: measures
tags: [okf, measure, price, pricing, list-price]
timestamp: 2026-07-28T00:00:00Z
---

# Unit List Price USD

## Business Definition

Unit List Price USD represents the standard list price per unit in U.S. dollars before discounts. This measure reflects the published or catalog price for products and services and is fundamental for pricing analysis, discount evaluation, and margin management.

---

## Technical Mapping

**Source Entity**: [Booking Fact](../entities/booking-fact.md)  
**Technical Column**: unit_list_price_usd  
**Data Type**: numeric(12,2)  
**Nullable**: Yes

---

## Measure Properties

**Aggregation Type**: Average  
**Measure Category**: Pricing Measure  
**Additive**: No (Semi-Additive)

---

## Formula

```
Average Unit List Price USD = AVG(unit_list_price_usd)
```

The measure is typically calculated as an average across booking transactions, as list prices vary by product and should not be summed.

---

## Related Entities

- [Booking Fact](../entities/booking-fact.md)
- [Product Dimension](../entities/product-dimension.md)

---

## Related Domains

- [Pricing](../domains/pricing.md)
- [Sales Transactions](../domains/sales-transactions.md)
- [Product Management](../domains/product-management.md)

---

## Business Rules

1. Unit List Price must be greater than or equal to zero
2. List prices should align with published product pricing
3. List prices are typically analyzed as averages, not sums
4. List prices may vary by product, customer segment, or geography
5. List prices represent pre-discount pricing

---

## Analytical Use Cases

- Track average list prices by product
- Analyze list price trends over time
- Compare list prices across product families
- Monitor list price changes and adjustments
- Support pricing strategy development
- Calculate price realization rates

---

## Related Measures

- [Discount Percentage](discount-percentage.md) - Discount applied to list price
- [Booking Amount USD](booking-amount-usd.md) - Net revenue after discounts
- [Quantity Sold](quantity-sold.md) - Volume sold at list price

---

## Calculation Examples

### Average Unit List Price
```
AVG(unit_list_price_usd)
```

### Weighted Average List Price
```
SUM(unit_list_price_usd * quantity) / SUM(quantity)
```

### List Price by Product
```
AVG(unit_list_price_usd) GROUP BY product_name
```

### Effective Price
```
unit_list_price_usd * (1 - discount_pct/100)
```

---

## Navigation

- [Back to Measures Index](index.md)
- [Back to Bundle Index](../index.md)
