---
title: Distinct Order Count
type: measure
description: Count of distinct sales orders associated with booking transactions
resource: measures
tags: [order-count, volume, metric, count]
timestamp: 2026-07-28T00:00:00Z
---

# Distinct Order Count

## Business Definition

Distinct Order Count represents the total number of unique sales orders associated with booking transactions. Since each sales order may contain multiple line items (booking transactions), this measure provides a count of distinct orders rather than individual booking lines.

---

## Formula

**Expression**: COUNT(DISTINCT bookings.order_number)

**Dialect**: ANSI_SQL

**Aggregation Type**: COUNT DISTINCT

---

## Business Purpose

This measure enables:

- **Order Volume Tracking**: Monitor the number of unique sales orders processed
- **Order vs Line Analysis**: Compare order count to booking count to understand order complexity
- **Order Consolidation**: Track average number of line items per order
- **Order Processing**: Support operational metrics for order processing efficiency
- **Customer Behavior**: Analyze ordering patterns and order sizes

---

## Related Entities

**Primary Entity**: [Bookings](../entities/bookings.md)

**Dimensional Analysis**: This measure can be analyzed across all dimension entities:
- [Customers](../entities/customers.md) - Order count by customer segment, industry, account tier
- [Products](../entities/products.md) - Order count by product family, technology domain
- [Partners](../entities/partners.md) - Order count by partner type, tier
- [Geographies](../entities/geographies.md) - Order count by region, theater, country
- [Sales Representatives](../entities/sales-representatives.md) - Order count by sales role, team
- [Contracts](../entities/contracts.md) - Order count by contract type
- [Dates](../entities/dates.md) - Order count by fiscal year, quarter, month

---

## Related Concepts

- [Sales Order](../glossary/sales-order.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Calculation Logic

The measure counts each unique order_number in the bookings fact table. Multiple booking records with the same order_number are counted only once, representing a single sales order with multiple line items.

---

## Usage Examples

### Monthly Order Volume
```sql
SELECT 
    dates.fiscal_year,
    dates.month_name,
    COUNT(DISTINCT bookings.order_number) as order_count
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.fiscal_year, dates.month_name
```

### Average Lines per Order
```sql
SELECT 
    COUNT(bookings.booking_id) / NULLIF(COUNT(DISTINCT bookings.order_number), 0) as avg_lines_per_order
FROM bookings
```

---

## Business Rules

1. **Distinct Counting**: Each order is counted only once regardless of the number of line items
2. **Order Identification**: order_number uniquely identifies a sales order
3. **Multi-Line Orders**: Orders with multiple products or services will have multiple booking records but count as one order

---

## Related Measures

- [Booking Count](./booking-count.md) - Count of individual booking transactions
- [Total Booking Amount USD](./total-booking-amount-usd.md) - Total revenue from bookings
- [Average Booking Value USD](./average-booking-value-usd.md) - Average value per booking transaction

---

## Derived Metrics

### Average Lines per Order
```
Booking Count / Distinct Order Count
```

### Average Order Value
```
Total Booking Amount USD / Distinct Order Count
```

---

## Data Quality Considerations

- Ensure order_number is populated for all booking records
- Verify order_number consistency across related booking lines
- Confirm order_number format and uniqueness

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
