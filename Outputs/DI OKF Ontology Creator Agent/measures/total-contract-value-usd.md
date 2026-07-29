---
title: Total Contract Value USD
type: measure
description: Total contract value in U.S. dollars over the full contract term
resource: measures
tags: [okf, measure, tcv, revenue, contract]
timestamp: 2026-07-28T00:00:00Z
---

# Total Contract Value USD

## Business Definition

Total Contract Value USD (TCV) represents the total contract value in U.S. dollars over the full contract term. TCV captures the complete value of the contract over its entire duration and is fundamental for analyzing long-term contract value, deal size, and contract profitability.

---

## Technical Mapping

**Source Entity**: [Booking Fact](../entities/booking-fact.md)  
**Technical Column**: tcv_usd  
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
Total Contract Value USD = SUM(tcv_usd)
```

The measure is calculated by summing the TCV values across all booking transactions within the selected scope.

**Relationship to ACV**:
```
For multi-year contracts: tcv_usd = acv_usd * (term_months / 12)
For 1-year contracts: tcv_usd = acv_usd = booking_amount_usd
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

1. TCV must be greater than or equal to zero
2. TCV aggregates additively across all dimensions
3. TCV must be greater than or equal to ACV
4. For 1-year contracts, TCV should equal ACV and Booking Amount
5. For multi-year contracts, TCV represents full contract term value

---

## Analytical Use Cases

- Analyze long-term contract value by segment
- Track average deal size trends
- Compare contract values across dimensions
- Identify large deal opportunities
- Support contract value forecasting
- Measure total contract portfolio value
- Evaluate contract profitability

---

## Related Measures

- [Annual Contract Value USD](annual-contract-value-usd.md) - Annualized recurring revenue
- [Booking Amount USD](booking-amount-usd.md) - Total transaction value
- [Quantity Sold](quantity-sold.md) - Volume component

---

## Calculation Examples

### Total Contract Value
```
SUM(tcv_usd)
```

### Average TCV per Deal
```
SUM(tcv_usd) / COUNT(booking_id)
```

### TCV by Customer Segment
```
SUM(tcv_usd) GROUP BY customer_segment
```

### TCV to ACV Ratio
```
SUM(tcv_usd) / SUM(acv_usd)
```

### Average Contract Term (in years)
```
SUM(tcv_usd) / SUM(acv_usd)
```

---

## Navigation

- [Back to Measures Index](index.md)
- [Back to Bundle Index](../index.md)
