---
title: Booking Count
type: measure
description: Count of booking transaction records
resource: measures
tags: [booking-count, volume, metric, count]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Count

## Business Definition

Booking Count represents the total number of individual booking transaction records. This measure provides a simple count of all booking transactions, enabling volume-based analysis of sales activity across all dimensions.

---

## Formula

**Expression**: COUNT(bookings.booking_id)

**Dialect**: ANSI_SQL

**Aggregation Type**: COUNT

---

## Business Purpose

This measure enables:

- **Transaction Volume Tracking**: Monitor the total number of booking transactions processed
- **Activity Analysis**: Track sales activity levels over time
- **Productivity Metrics**: Measure sales representative productivity by transaction count
- **Trend Analysis**: Identify booking volume trends and patterns
- **Capacity Planning**: Support operational capacity planning based on transaction volumes

---

## Related Entities

**Primary Entity**: [Bookings](../entities/bookings.md)

**Dimensional Analysis**: This measure can be analyzed across all dimension entities:
- [Customers](../entities/customers.md) - Booking count by customer segment, industry, account tier
- [Products](../entities/products.md) - Booking count by product family, technology domain, offer type
- [Partners](../entities/partners.md) - Booking count by partner type, tier, route to market
- [Geographies](../entities/geographies.md) - Booking count by region, theater, country
- [Sales Representatives](../entities/sales-representatives.md) - Booking count by sales role, team, segment
- [Contracts](../entities/contracts.md) - Booking count by contract type, term, coverage level
- [Dates](../entities/dates.md) - Booking count by fiscal year, quarter, month

---

## Related Concepts

- [Booking Transaction](../glossary/booking-transaction.md)
- [Sales Order](../glossary/sales-order.md)

---

## Calculation Logic

The measure counts each unique booking_id in the bookings fact table. Each booking transaction is counted exactly once, regardless of the booking amount or quantity.

---

## Usage Examples

### Monthly Booking Volume
```sql
SELECT 
    dates.fiscal_year,
    dates.month_name,
    COUNT(bookings.booking_id) as booking_count
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.fiscal_year, dates.month_name
```

### Booking Count by Sales Representative
```sql
SELECT 
    sales_representatives.rep_name,
    COUNT(bookings.booking_id) as booking_count
FROM bookings
JOIN sales_representatives ON bookings.sales_rep_key = sales_representatives.sales_rep_key
GROUP BY sales_representatives.rep_name
ORDER BY booking_count DESC
```

---

## Business Rules

1. **Unique Counting**: Each booking transaction is counted exactly once based on booking_id
2. **No Filtering**: All booking records are included in the count regardless of amount or status
3. **Null Handling**: booking_id is a required field and should never be null

---

## Related Measures

- [Distinct Order Count](./distinct-order-count.md) - Count of unique sales orders
- [Total Quantity](./total-quantity.md) - Total units booked
- [Total Booking Amount USD](./total-booking-amount-usd.md) - Total revenue from bookings
- [Average Booking Value USD](./average-booking-value-usd.md) - Average value per booking

---

## Data Quality Considerations

- Ensure booking_id is unique and not null
- Verify no duplicate booking records exist
- Confirm all booking transactions are captured in the fact table

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
