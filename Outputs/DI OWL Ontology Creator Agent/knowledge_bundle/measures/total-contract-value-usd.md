---
title: Total Contract Value USD
type: measure
description: Total value of the full contract associated with the booking in U.S. dollars
resource: measures
tags: [tcv, contract, total, financial, metric]
timestamp: 2026-07-28T00:00:00Z
---

# Total Contract Value USD

## Business Definition

Total value of the full contract associated with the booking in U.S. dollars. This measure represents the complete value of a contract over its entire term, providing visibility into long-term revenue commitments.

---

## Measure Identifier

**Measure ID:** MEA006  
**Source Entity:** [Booking Transaction](../entities/booking-transaction.md)

---

## Technical Mapping

**Source Table:** QuoteToBooking.fact_bookings  
**Source Column:** tcv_usd  
**Data Type:** Numeric

---

## Aggregation

**Aggregation Type:** SUM  
**Business Logic:** Sum of all total contract values across selected transactions

---

## Business Formula

```
Total Contract Value = SUM(tcv_usd)
TCV = Annual Contract Value × Contract Term (in years)
```

---

## Related Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Source entity for this measure
- **[Contract](../entities/contract.md)** - Contracts with total values
- **[Customer](../entities/customer.md)** - Customers with contract commitments
- **[Product](../entities/product.md)** - Products with contract values
- **[Partner](../entities/partner.md)** - Partners facilitating contracts

---

## Related Domains

- **[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)** - Primary domain

---

## Business Use Cases

1. **Long-term Value Analysis** - Track total committed revenue from contracts
2. **Contract Portfolio** - Analyze total value of active contract portfolio
3. **Revenue Pipeline** - Project future revenue from existing contracts
4. **Customer Lifetime Value** - Calculate total contract value per customer
5. **Strategic Planning** - Support long-term revenue planning and forecasting

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

- [Annual Contract Value USD](./annual-contract-value-usd.md) - Annualized contract value
- [Booking Amount USD](./booking-amount-usd.md) - Initial booking revenue
- [Quantity Sold](./quantity-sold.md) - Volume of contract commitments

---

## Calculated Relationships

```
Annual Contract Value = Total Contract Value / Contract Term (in years)
Contract Portfolio Value = SUM(Total Contract Value) for active contracts
```

---

## Key Performance Indicators

- Total Contract Value by Fiscal Year
- TCV Growth Rate
- Average TCV per Customer
- TCV by Contract Term Length
- New TCV vs Renewal TCV

---

## Glossary Reference

- [Total Contract Value USD](../glossary/total-contract-value-usd.md)

---

## Navigation

- [Return to Measures Index](./index.md)
- [View Metrics Summary](../metrics.md)
- [View Source Entity](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
