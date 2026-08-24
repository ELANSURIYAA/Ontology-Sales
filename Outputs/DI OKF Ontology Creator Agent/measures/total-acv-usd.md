---
title: Total ACV USD
type: measure
description: Total annual contract value in US dollars
resource: measures
tags: [acv, revenue, metric, annual-contract-value, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Total ACV USD

## Business Definition

Total ACV USD represents the total annual contract value in US dollars. ACV is the annualized revenue value of contracts, providing a normalized view of contract value for subscription and recurring revenue analysis. This measure is essential for tracking recurring revenue and subscription business performance.

---

## Formula

**Expression**: SUM(bookings.acv_usd)

**Dialect**: ANSI_SQL

**Aggregation Type**: SUM

---

## Business Purpose

This measure enables:

- **Recurring Revenue Tracking**: Monitor annual recurring revenue (ARR) from contracts
- **Subscription Analysis**: Track subscription business performance
- **Revenue Forecasting**: Project future revenue based on annualized contract values
- **Growth Metrics**: Calculate year-over-year ACV growth
- **Valuation Metrics**: Support business valuation based on recurring revenue
- **Investor Reporting**: Provide key metrics for investor and board reporting

---

## Related Entities

**Primary Entity**: [Bookings](../entities/bookings.md)

**Dimensional Analysis**: This measure can be analyzed across all dimension entities:
- [Customers](../entities/customers.md) - ACV by customer segment, industry, account tier
- [Products](../entities/products.md) - ACV by product family, technology domain, offer type
- [Partners](../entities/partners.md) - ACV by partner type, tier, route to market
- [Geographies](../entities/geographies.md) - ACV by region, theater, country
- [Sales Representatives](../entities/sales-representatives.md) - ACV by sales role, team, segment
- [Contracts](../entities/contracts.md) - ACV by contract type, term, coverage level
- [Dates](../entities/dates.md) - ACV by fiscal year, quarter, month

---

## Related Concepts

- [Annual Contract Value](../glossary/annual-contract-value.md)
- [Total Contract Value](../glossary/total-contract-value.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Calculation Logic

The measure sums the acv_usd field from all booking records. ACV represents the annualized value of the contract, calculated by dividing the total contract value by the contract term in years:

```
acv_usd = tcv_usd / (term_months / 12)
```

For annual contracts, ACV equals the booking amount. For multi-year contracts, ACV represents the annual portion of the total contract value.

---

## Usage Examples

### Fiscal Year ACV
```sql
SELECT 
    dates.fiscal_year,
    SUM(bookings.acv_usd) as total_acv
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.fiscal_year
```

### ACV by Product Family
```sql
SELECT 
    products.product_family,
    SUM(bookings.acv_usd) as total_acv
FROM bookings
JOIN products ON bookings.product_key = products.product_key
GROUP BY products.product_family
ORDER BY total_acv DESC
```

---

## Business Rules

1. **Non-Negative Values**: ACV must be non-negative
2. **Currency**: All amounts are in US dollars
3. **Annualization**: ACV represents the annual portion of contract value
4. **Additive Measure**: ACV can be summed across all dimensions
5. **Subscription Focus**: Most relevant for subscription and recurring revenue contracts

---

## Related Measures

- [Total Booking Amount USD](./total-booking-amount-usd.md) - Total booking revenue
- [Total TCV USD](./total-tcv-usd.md) - Total contract value over full term
- [Renewal Booking Amount USD](./renewal-booking-amount-usd.md) - Renewal revenue
- [Net New Booking Amount USD](./net-new-booking-amount-usd.md) - Net new revenue

---

## Derived Metrics

### ACV to TCV Ratio
```
Total ACV USD / Total TCV USD
```

### Average Contract Term (in years)
```
Total TCV USD / Total ACV USD
```

### ACV Growth Rate
```
(Current Period ACV - Prior Period ACV) / Prior Period ACV
```

---

## Data Quality Considerations

- Ensure acv_usd is non-negative and not null
- Verify ACV calculation is consistent with TCV and contract term
- Confirm ACV is properly annualized for multi-year contracts
- Validate ACV values are within reasonable ranges

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
