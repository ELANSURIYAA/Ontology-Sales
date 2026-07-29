---
title: Quantity Sold
type: measure
description: Number of units, licenses, or subscriptions booked in the transaction
resource: measures
tags: [okf, measure, quantity, volume, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Quantity Sold

## Business Definition

Quantity Sold represents the number of units, licenses, or subscriptions booked in the transaction. This measure tracks the volume of products or services sold and is fundamental for analyzing sales velocity, product adoption, and demand patterns.

---

## Technical Mapping

**Source Entity**: [Booking Fact](../entities/booking-fact.md)  
**Technical Column**: quantity  
**Data Type**: integer  
**Nullable**: Yes

---

## Measure Properties

**Aggregation Type**: Sum  
**Measure Category**: Volume Measure  
**Additive**: Yes

---

## Formula

```
Quantity Sold = SUM(quantity)
```

The measure is calculated by summing the quantity values across all booking transactions within the selected scope.

---

## Related Entities

- [Booking Fact](../entities/booking-fact.md)

---

## Related Domains

- [Sales Transactions](../domains/sales-transactions.md)
- [Product Management](../domains/product-management.md)

---

## Business Rules

1. Quantity must be greater than zero for valid bookings
2. Quantity represents discrete units (integer values)
3. Quantity aggregates additively across all dimensions
4. Null quantities should be treated as zero or excluded from analysis

---

## Analytical Use Cases

- Track total units sold by time period
- Analyze product demand and adoption rates
- Measure sales velocity and transaction frequency
- Compare volume across products, customers, and geographies
- Support inventory planning and demand forecasting
- Calculate average quantity per transaction

---

## Related Measures

- [Booking Amount USD](booking-amount-usd.md) - Revenue value of quantities sold
- [Unit List Price USD](unit-list-price-usd.md) - Price per unit sold
- [Discount Percentage](discount-percentage.md) - Discount applied to quantities

---

## Calculation Examples

### Total Quantity Sold
```
SUM(quantity) across all bookings
```

### Average Quantity per Booking
```
SUM(quantity) / COUNT(booking_id)
```

### Quantity by Product
```
SUM(quantity) GROUP BY product_name
```

---

## Navigation

- [Back to Measures Index](index.md)
- [Back to Bundle Index](../index.md)
