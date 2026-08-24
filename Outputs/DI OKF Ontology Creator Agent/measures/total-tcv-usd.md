---
title: Total TCV USD
type: measure
description: Total contract value in US dollars
resource: measures
tags: [tcv, revenue, metric, total-contract-value, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Total TCV USD

## Business Definition

Total TCV USD represents the total contract value in US dollars over the full contract term. TCV captures the complete revenue value expected from a contract over its entire duration, providing a comprehensive view of long-term revenue commitments.

---

## Formula

**Expression**: SUM(bookings.tcv_usd)

**Dialect**: ANSI_SQL

**Aggregation Type**: SUM

---

## Business Purpose

This measure enables:

- **Long-Term Revenue Planning**: Track total committed revenue over contract lifetimes
- **Contract Value Analysis**: Evaluate total contract values across dimensions
- **Revenue Forecasting**: Project long-term revenue based on contract commitments
- **Deal Size Analysis**: Analyze average deal sizes and contract values
- **Multi-Year Tracking**: Monitor multi-year contract performance
- **Pipeline Valuation**: Support pipeline and opportunity valuation

---

## Related Entities

**Primary Entity**: [Bookings](../entities/bookings.md)

**Dimensional Analysis**: This measure can be analyzed across all dimension entities:
- [Customers](../entities/customers.md) - TCV by customer segment, industry, account tier
- [Products](../entities/products.md) - TCV by product family, technology domain, offer type
- [Partners](../entities/partners.md) - TCV by partner type, tier, route to market
- [Geographies](../entities/geographies.md) - TCV by region, theater, country
- [Sales Representatives](../entities/sales-representatives.md) - TCV by sales role, team, segment
- [Contracts](../entities/contracts.md) - TCV by contract type, term, coverage level
- [Dates](../entities/dates.md) - TCV by fiscal year, quarter, month

---

## Related Concepts

- [Total Contract Value](../glossary/total-contract-value.md)
- [Annual Contract Value](../glossary/annual-contract-value.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Calculation Logic

The measure sums the tcv_usd field from all booking records. TCV represents the total revenue value over the full contract term:

```
tcv_usd = acv_usd × (term_months / 12)
```

For annual contracts, TCV equals the booking amount. For multi-year contracts, TCV represents the total value across all years.

---

## Usage Examples

### Fiscal Year TCV
```sql
SELECT 
    dates.fiscal_year,
    SUM(bookings.tcv_usd) as total_tcv
FROM bookings
JOIN dates ON bookings.date_key = dates.date_key
GROUP BY dates.fiscal_year
```

### TCV by Contract Type
```sql
SELECT 
    contracts.contract_type,
    SUM(bookings.tcv_usd) as total_tcv
FROM bookings
JOIN contracts ON bookings.contract_key = contracts.contract_key
GROUP BY contracts.contract_type
ORDER BY total_tcv DESC
```

---

## Business Rules

1. **Non-Negative Values**: TCV must be non-negative
2. **Currency**: All amounts are in US dollars
3. **Full Term Value**: TCV represents total value over complete contract term
4. **Additive Measure**: TCV can be summed across all dimensions
5. **Multi-Year Contracts**: TCV is particularly relevant for multi-year agreements

---

## Related Measures

- [Total Booking Amount USD](./total-booking-amount-usd.md) - Total booking revenue
- [Total ACV USD](./total-acv-usd.md) - Annual contract value
- [Renewal Booking Amount USD](./renewal-booking-amount-usd.md) - Renewal revenue
- [Net New Booking Amount USD](./net-new-booking-amount-usd.md) - Net new revenue

---

## Derived Metrics

### Average Contract Term (in years)
```
Total TCV USD / Total ACV USD
```

### Average TCV per Booking
```
Total TCV USD / Booking Count
```

### TCV to Booking Amount Ratio
```
Total TCV USD / Total Booking Amount USD
```

---

## Data Quality Considerations

- Ensure tcv_usd is non-negative and not null
- Verify TCV calculation is consistent with ACV and contract term
- Confirm TCV properly reflects multi-year contract values
- Validate TCV values are within reasonable ranges

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
