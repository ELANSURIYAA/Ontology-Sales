---
title: Annual Contract Value USD
type: measure
description: Annualized value of the contract associated with the booking in U.S. dollars
resource: measures
tags: [measure, acv, contract-value, revenue, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Annual Contract Value USD

## Business Definition

Annualized value of the contract associated with the booking in U.S. dollars.

---

## Technical Mapping

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Technical Column**: acv_usd

**Data Type**: Numeric

**Aggregation Type**: SUM

---

## Formula

**Annual Contract Value (ACV)** represents the annualized value of the contract commitment.

For multi-year contracts:
**ACV** = Total Contract Value USD / (Contract Term Months / 12)

For annual contracts:
**ACV** = Total Contract Value USD

---

## Aggregation

**Default Aggregation**: SUM

**Valid Aggregations**:
- SUM: Total annualized contract value across all transactions
- AVG: Average ACV per transaction
- MIN: Minimum ACV
- MAX: Maximum ACV

---

## Related Entities

- [Booking Transaction](../entities/booking-transaction.md): Source entity for this measure
- [Customer](../entities/customer.md): Analyze ACV by customer attributes
- [Product](../entities/product.md): Analyze ACV by product attributes
- [Partner](../entities/partner.md): Analyze ACV by partner attributes
- [Geography](../entities/geography.md): Analyze ACV by geographic attributes
- [Sales Representative](../entities/sales-representative.md): Analyze ACV by sales representative
- [Contract](../entities/contract.md): Analyze ACV by contract attributes
- [Date](../entities/date.md): Analyze ACV trends over time

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. ACV represents the annualized value of the contract
2. All amounts are recorded in U.S. dollars
3. ACV normalizes multi-year contracts to annual values
4. Used for recurring revenue analysis and forecasting
5. Particularly relevant for subscription and SaaS business models
6. ACV enables year-over-year comparison regardless of contract term

---

## Usage Examples

**Recurring Revenue Analysis**:
- Calculate total annual recurring revenue
- Measure ACV growth trends
- Forecast future recurring revenue

**Customer ACV Analysis**:
- Identify high-value customers by ACV
- Measure average ACV by customer segment
- Analyze customer expansion through ACV growth

**Product ACV Analysis**:
- Evaluate subscription product performance
- Compare ACV across product families
- Measure SaaS adoption by ACV

**Contract Term Analysis**:
- Compare ACV for different contract terms
- Analyze multi-year vs. annual contracts
- Evaluate contract term preferences

**Sales Performance**:
- Track ACV quota attainment
- Measure average ACV by sales representative
- Analyze ACV deal size trends

---

## Related Measures

- [Booking Amount USD](booking-amount-usd.md): Total booking revenue
- [Total Contract Value USD](total-contract-value-usd.md): Full contract value
- [Quantity Sold](quantity-sold.md): Volume measure
- [Unit List Price USD](unit-list-price-usd.md): Base price
- [Discount Percentage](discount-percentage.md): Discount applied

---

## Related Concepts

- [Annual Contract Value USD](../glossary/annual-contract-value-usd.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Contract Term Months](../glossary/contract-term-months.md)

---

## Navigation

- [Back to Measures Index](index.md)
- [Back to Main Index](../index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [View Metrics](../metrics.md)
