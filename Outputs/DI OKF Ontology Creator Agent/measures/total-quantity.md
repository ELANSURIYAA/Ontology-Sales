---
title: Total Quantity
type: measure
description: Total number of units, licenses, or services booked
resource: measures
tags: [quantity, volume, metric, units]
timestamp: 2026-07-28T00:00:00Z
---

# Total Quantity

## Business Definition

Total Quantity represents the total number of units, licenses, or services booked across all booking transactions. This measure aggregates the quantity field from booking records to provide a comprehensive view of volume sold.

---

## Formula

**Expression**: SUM(bookings.quantity)

**Dialect**: ANSI_SQL

**Aggregation Type**: SUM

---

## Business Purpose

This measure enables:

- **Volume Analysis**: Track the total volume of products or services sold
- **Unit Sales Tracking**: Monitor unit sales trends over time
- **Capacity Planning**: Support inventory and capacity planning based on unit volumes
- **License Management**: Track software license or subscription quantities
- **Pricing Analysis**: Calculate average selling price per unit when combined with revenue measures

---

## Related Entities

**Primary Entity**: [Bookings](../entities/bookings.md)

**Dimensional Analysis**: This measure can be analyzed across all dimension entities:
- [Customers](../entities/customers.md) - Quantity by customer segment, industry, account tier
- [Products](../entities/products.md) - Quantity by product family, technology domain, offer type
- [Partners](../entities/partners.md) - Quantity by partner type, tier, route to market
- [Geographies](../entities/geographies.md) - Quantity by region, theater, country
- [Sales Representatives](../entities/sales-representatives.md) - Quantity by sales role, team
- [Contracts](../entities/contracts.md) - Quantity by contract type, term
- [Dates](../entities/dates.md) - Quantity by fiscal year, quarter, month

---

## Related Concepts

- [Booking Transaction](../glossary/booking-transaction.md)

---

## Calculation Logic

The measure sums the quantity field from all booking records. Each booking transaction contributes its quantity value to the total, representing the number of units, licenses, or services included in that transaction.

---

## Usage Examples

### Monthly Quantity Trends
```sql
SELECT 
    dates.fiscal_year,
    dates.month_name,
    SUM(bookings.quantity) as total_quantity
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.fiscal_year, dates.month_name
```

### Quantity by Product Family
```sql
SELECT 
    products.product_family,
    SUM(bookings.quantity) as total_quantity
FROM bookings
JOIN products ON bookings.product_key = products.product_key
GROUP BY products.product_family
ORDER BY total_quantity DESC
```

---

## Business Rules

1. **Positive Values**: Quantity must be a positive integer
2. **Unit Consistency**: Quantity represents units in the context of each product (licenses, devices, subscriptions, etc.)
3. **Additive Measure**: Quantities can be summed across all dimensions

---

## Related Measures

- [Booking Count](./booking-count.md) - Count of booking transactions
- [Total Booking Amount USD](./total-booking-amount-usd.md) - Total revenue from bookings
- [Average Selling Price USD](./average-selling-price-usd.md) - Average revenue per unit (calculated as Total Booking Amount / Total Quantity)

---

## Derived Metrics

### Average Selling Price per Unit
```
Total Booking Amount USD / Total Quantity
```

### Average Quantity per Booking
```
Total Quantity / Booking Count
```

---

## Data Quality Considerations

- Ensure quantity is always positive and not null
- Verify quantity values are reasonable for the product type
- Confirm quantity units are consistent within product categories

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
