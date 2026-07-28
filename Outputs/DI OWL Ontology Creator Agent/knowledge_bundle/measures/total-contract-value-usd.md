---
title: Total Contract Value USD
type: measure
description: Total value of the full contract associated with the booking in U.S. dollars
resource: measures
tags: [measure, tcv, contract-value, revenue, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Total Contract Value USD

## Business Definition

Total value of the full contract associated with the booking in U.S. dollars.

---

## Technical Mapping

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Technical Column**: tcv_usd

**Data Type**: Numeric

**Aggregation Type**: SUM

---

## Formula

**Total Contract Value (TCV)** represents the full value of the contract over its entire term.

**TCV** = Annual Contract Value USD × (Contract Term Months / 12)

For single-period bookings:
**TCV** = Booking Amount USD

---

## Aggregation

**Default Aggregation**: SUM

**Valid Aggregations**:
- SUM: Total contract value across all transactions
- AVG: Average TCV per transaction
- MIN: Minimum TCV
- MAX: Maximum TCV

---

## Related Entities

- [Booking Transaction](../entities/booking-transaction.md): Source entity for this measure
- [Customer](../entities/customer.md): Analyze TCV by customer attributes
- [Product](../entities/product.md): Analyze TCV by product attributes
- [Partner](../entities/partner.md): Analyze TCV by partner attributes
- [Geography](../entities/geography.md): Analyze TCV by geographic attributes
- [Sales Representative](../entities/sales-representative.md): Analyze TCV by sales representative
- [Contract](../entities/contract.md): Analyze TCV by contract attributes
- [Date](../entities/date.md): Analyze TCV trends over time

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. TCV represents the total value of the full contract commitment
2. All amounts are recorded in U.S. dollars
3. TCV includes the entire contract term value
4. Used for total commitment and pipeline analysis
5. TCV is higher than ACV for multi-year contracts
6. TCV represents the customer's total financial commitment

---

## Usage Examples

**Contract Value Analysis**:
- Calculate total contract commitments
- Measure TCV growth trends
- Analyze total customer commitment

**Customer TCV Analysis**:
- Identify largest contract commitments by customer
- Measure total customer lifetime commitment
- Analyze TCV by customer segment

**Product TCV Analysis**:
- Evaluate total product contract value
- Compare TCV across product families
- Measure long-term product commitment

**Contract Term Analysis**:
- Compare TCV for different contract terms
- Analyze multi-year contract value
- Evaluate contract term preferences by TCV

**Sales Performance**:
- Track TCV quota attainment
- Measure total deal value by sales representative
- Analyze large deal performance

**Pipeline Analysis**:
- Forecast total contract value in pipeline
- Measure TCV conversion rates
- Analyze deal size distribution

---

## Related Measures

- [Booking Amount USD](booking-amount-usd.md): Total booking revenue
- [Annual Contract Value USD](annual-contract-value-usd.md): Annualized contract value
- [Quantity Sold](quantity-sold.md): Volume measure
- [Unit List Price USD](unit-list-price-usd.md): Base price
- [Discount Percentage](discount-percentage.md): Discount applied

---

## Related Concepts

- [Total Contract Value USD](../glossary/total-contract-value-usd.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Contract Term Months](../glossary/contract-term-months.md)

---

## Navigation

- [Back to Measures Index](index.md)
- [Back to Main Index](../index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [View Metrics](../metrics.md)
