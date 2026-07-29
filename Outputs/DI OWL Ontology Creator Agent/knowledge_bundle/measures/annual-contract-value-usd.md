---
title: Annual Contract Value USD
type: measure
description: Annualized value of the contract associated with the booking in U.S. dollars
resource: measures
tags: [acv, contract, annual, financial, metric]
timestamp: 2026-07-28T00:00:00Z
---

# Annual Contract Value USD

## Business Definition

Annualized value of the contract associated with the booking in U.S. dollars. This measure represents the yearly value of a contract, normalizing multi-year agreements to an annual basis for consistent comparison and analysis.

---

## Measure Identifier

**Measure ID:** MEA005  
**Source Entity:** [Booking Transaction](../entities/booking-transaction.md)

---

## Technical Mapping

**Source Table:** QuoteToBooking.fact_bookings  
**Source Column:** acv_usd  
**Data Type:** Numeric

---

## Aggregation

**Aggregation Type:** SUM  
**Business Logic:** Sum of all annual contract values across selected transactions

---

## Business Formula

```
Total Annual Contract Value = SUM(acv_usd)
ACV = Total Contract Value / Contract Term (in years)
```

---

## Related Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Source entity for this measure
- **[Contract](../entities/contract.md)** - Contracts with annual values
- **[Customer](../entities/customer.md)** - Customers with annual contract commitments
- **[Product](../entities/product.md)** - Products with annual contract values
- **[Partner](../entities/partner.md)** - Partners facilitating annual contracts

---

## Related Domains

- **[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)** - Primary domain

---

## Business Use Cases

1. **Subscription Analysis** - Track annual recurring revenue from subscriptions
2. **Contract Comparison** - Compare contracts of different term lengths on annual basis
3. **Revenue Forecasting** - Project annual revenue from contract commitments
4. **Customer Value** - Analyze annual customer value and retention
5. **Growth Tracking** - Monitor annual contract value growth over time

---

## Analysis Dimensions

This measure can be analyzed across:

- [Customer](../entities/customer.md) - Segment, industry, account tier
- [Product](../entities/product.md) - Product family, technology domain, offer type
- [Partner](../entities/partner.md) - Partner type, partner tier
- [Geography](../entities/geography.md) - Region, theater, country
- [Date](../entities/date.md) - Fiscal year, quarter, period
- [Sales Representative](../entities/sales-representative.md) - Sales role, team
- [Contract](../entities/contract.md) - Contract type, term, coverage level

---

## Related Measures

- [Total Contract Value USD](./total-contract-value-usd.md) - Total contract value over full term
- [Booking Amount USD](./booking-amount-usd.md) - Initial booking revenue
- [Quantity Sold](./quantity-sold.md) - Volume of annual subscriptions

---

## Calculated Relationships

```
Total Contract Value = Annual Contract Value × Contract Term (in years)
Annual Recurring Revenue = SUM(Annual Contract Value) for active contracts
```

---

## Key Performance Indicators

- Total Annual Contract Value by Fiscal Year
- ACV Growth Rate
- Average ACV per Customer
- ACV by Product Family
- New ACV vs Renewal ACV

---

## Glossary Reference

- [Annual Contract Value USD](../glossary/annual-contract-value-usd.md)

---

## Navigation

- [Return to Measures Index](./index.md)
- [View Metrics Summary](../metrics.md)
- [View Source Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
