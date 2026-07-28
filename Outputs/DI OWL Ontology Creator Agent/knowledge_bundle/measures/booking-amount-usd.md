---
title: Booking Amount USD
type: measure
description: Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments
resource: measures
tags: [measure, revenue, booking, amount, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Amount USD

## Business Definition

Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments.

---

## Technical Mapping

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Technical Column**: booking_amount_usd

**Data Type**: Numeric

**Aggregation Type**: SUM

---

## Formula

**Booking Amount USD** = (Unit List Price USD × Quantity Sold) × (1 - Discount Percentage)

This represents the net revenue after applying discounts to the list price.

---

## Aggregation

**Default Aggregation**: SUM

**Valid Aggregations**:
- SUM: Total booking revenue across all transactions
- AVG: Average booking amount per transaction
- MIN: Minimum booking amount
- MAX: Maximum booking amount
- COUNT: Number of transactions with booking amounts

---

## Related Entities

- [Booking Transaction](../entities/booking-transaction.md): Source entity for this measure
- [Customer](../entities/customer.md): Analyze booking revenue by customer attributes
- [Product](../entities/product.md): Analyze booking revenue by product attributes
- [Partner](../entities/partner.md): Analyze booking revenue by partner attributes
- [Geography](../entities/geography.md): Analyze booking revenue by geographic attributes
- [Sales Representative](../entities/sales-representative.md): Analyze booking revenue by sales representative
- [Contract](../entities/contract.md): Analyze booking revenue by contract attributes
- [Date](../entities/date.md): Analyze booking revenue trends over time

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. Booking Amount USD is the primary revenue metric
2. All amounts are recorded in U.S. dollars
3. Booking amount reflects net revenue after discounts
4. Aggregation is typically SUM to calculate total revenue
5. Used for revenue reporting, forecasting, and performance analysis
6. Represents completed bookings only

---

## Usage Examples

**Revenue Analysis**:
- Calculate total booking revenue by fiscal period
- Measure year-over-year revenue growth
- Track revenue against targets

**Customer Revenue Analysis**:
- Identify top customers by booking revenue
- Measure revenue by customer segment
- Calculate customer lifetime value

**Product Revenue Analysis**:
- Evaluate product family contribution to revenue
- Analyze product mix by revenue
- Identify top-performing products

**Geographic Revenue Analysis**:
- Compare revenue by sales region
- Analyze revenue distribution by country
- Measure geographic market performance

**Partner Revenue Analysis**:
- Evaluate partner contribution to revenue
- Compare direct vs. indirect revenue
- Measure channel effectiveness

**Sales Performance**:
- Track sales representative quota attainment
- Measure team revenue contribution
- Analyze average deal size

---

## Related Measures

- [Annual Contract Value USD](annual-contract-value-usd.md): Annualized contract value
- [Total Contract Value USD](total-contract-value-usd.md): Full contract value
- [Quantity Sold](quantity-sold.md): Volume measure
- [Unit List Price USD](unit-list-price-usd.md): Base price before discount
- [Discount Percentage](discount-percentage.md): Discount applied to price

---

## Related Concepts

- [Booking Amount USD](../glossary/booking-amount-usd.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [Back to Measures Index](index.md)
- [Back to Main Index](../index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [View Metrics](../metrics.md)
