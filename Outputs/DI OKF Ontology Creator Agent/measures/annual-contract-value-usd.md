---
title: Annual Contract Value USD
type: measure
description: Annualized contract value in U.S. dollars used for recurring revenue analysis
resource: measures
tags: [okf, measure, acv, revenue, recurring]
timestamp: 2026-07-28T00:00:00Z
---

# Annual Contract Value USD

## Business Definition

Annual Contract Value USD (ACV) represents the annualized contract value in U.S. dollars used for recurring revenue analysis. ACV normalizes contract values to an annual basis, enabling consistent comparison of contracts with different terms and supporting recurring revenue forecasting.

---

## Technical Mapping

**Source Entity**: [Booking Fact](../entities/booking-fact.md)  
**Technical Column**: acv_usd  
**Data Type**: numeric(14,2)  
**Nullable**: Yes

---

## Measure Properties

**Aggregation Type**: Sum  
**Measure Category**: Revenue Measure  
**Additive**: Yes

---

## Formula

```
Annual Contract Value USD = SUM(acv_usd)
```

The measure is calculated by summing the ACV values across all booking transactions within the selected scope.

**Calculation Logic**:
```
For multi-year contracts: acv_usd = tcv_usd / (term_months / 12)
For 1-year contracts: acv_usd = booking_amount_usd
```

---

## Related Entities

- [Booking Fact](../entities/booking-fact.md)
- [Contract Dimension](../entities/contract-dimension.md)
- [Customer Dimension](../entities/customer-dimension.md)
- [Product Dimension](../entities/product-dimension.md)

---

## Related Domains

- [Revenue Metrics](../domains/revenue-metrics.md)
- [Sales Transactions](../domains/sales-transactions.md)
- [Contract Management](../domains/contract-management.md)

---

## Business Rules

1. ACV must be greater than or equal to zero
2. ACV aggregates additively across all dimensions
3. For 1-year contracts, ACV should equal Booking Amount
4. For multi-year contracts, ACV represents annualized value
5. ACV should be less than or equal to Total Contract Value

---

## Analytical Use Cases

- Monitor recurring revenue trends
- Analyze subscription revenue growth
- Track ACV by customer segment and product
- Support recurring revenue forecasting
- Compare contract values on normalized annual basis
- Measure subscription business performance
- Calculate customer lifetime value

---

## Related Measures

- [Total Contract Value USD](total-contract-value-usd.md) - Full contract term value
- [Booking Amount USD](booking-amount-usd.md) - Total transaction value
- [Quantity Sold](quantity-sold.md) - Volume component

---

## Calculation Examples

### Total Annual Contract Value
```
SUM(acv_usd)
```

### Average ACV per Customer
```
SUM(acv_usd) / COUNT(DISTINCT customer_key)
```

### ACV by Product Family
```
SUM(acv_usd) GROUP BY product_family
```

### ACV to TCV Ratio
```
SUM(acv_usd) / SUM(tcv_usd)
```

### ACV Growth Rate
```
(Current Period ACV - Prior Period ACV) / Prior Period ACV
```

---

## Navigation

- [Back to Measures Index](index.md)
- [Back to Bundle Index](../index.md)
