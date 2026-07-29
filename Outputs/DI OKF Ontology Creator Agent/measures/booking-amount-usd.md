---
title: Booking Amount USD
type: measure
description: Total booked revenue amount in U.S. dollars for the transaction
resource: measures
tags: [okf, measure, revenue, booking, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Amount USD

## Business Definition

Booking Amount USD represents the total booked revenue amount in U.S. dollars for the transaction. This is the primary revenue measure for sales performance analysis and represents the net value of the booking after applying discounts to the list price.

---

## Technical Mapping

**Source Entity**: [Booking Fact](../entities/booking-fact.md)  
**Technical Column**: booking_amount_usd  
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
Booking Amount USD = SUM(booking_amount_usd)
```

The measure is calculated by summing the booking amount values across all booking transactions within the selected scope.

**Calculation Logic**:
```
booking_amount_usd = quantity * unit_list_price_usd * (1 - discount_pct/100)
```

---

## Related Entities

- [Booking Fact](../entities/booking-fact.md)
- [Customer Dimension](../entities/customer-dimension.md)
- [Product Dimension](../entities/product-dimension.md)
- [Date Dimension](../entities/date-dimension.md)

---

## Related Domains

- [Revenue Metrics](../domains/revenue-metrics.md)
- [Sales Transactions](../domains/sales-transactions.md)
- [Pricing](../domains/pricing.md)

---

## Business Rules

1. Booking Amount must be greater than or equal to zero
2. Booking Amount aggregates additively across all dimensions
3. Booking Amount should equal Quantity × Unit List Price × (1 - Discount %)
4. Booking Amount represents net revenue at time of booking
5. Null booking amounts should be treated as zero or excluded from analysis

---

## Analytical Use Cases

- Track total booking revenue by time period
- Analyze revenue growth trends
- Compare actual bookings to targets and quotas
- Measure revenue contribution by dimension (customer, product, partner, geography)
- Support revenue forecasting and planning
- Calculate average deal size
- Evaluate sales representative performance

---

## Related Measures

- [Annual Contract Value USD](annual-contract-value-usd.md) - Annualized recurring revenue
- [Total Contract Value USD](total-contract-value-usd.md) - Full contract term value
- [Quantity Sold](quantity-sold.md) - Volume component of booking amount
- [Unit List Price USD](unit-list-price-usd.md) - Price component before discount
- [Discount Percentage](discount-percentage.md) - Discount applied to calculate booking amount

---

## Calculation Examples

### Total Booking Amount
```
SUM(booking_amount_usd)
```

### Average Deal Size
```
SUM(booking_amount_usd) / COUNT(booking_id)
```

### Booking Amount by Product
```
SUM(booking_amount_usd) GROUP BY product_name
```

### Year-over-Year Growth
```
(Current Year Booking Amount - Prior Year Booking Amount) / Prior Year Booking Amount
```

---

## Navigation

- [Back to Measures Index](index.md)
- [Back to Bundle Index](../index.md)
