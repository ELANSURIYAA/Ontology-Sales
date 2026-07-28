---
title: Discount Percentage
type: measure
description: Percentage discount applied to the list price for the booking transaction
resource: measures
tags: [measure, discount, pricing, percentage]
timestamp: 2026-07-28T00:00:00Z
---

# Discount Percentage

## Business Definition

Percentage discount applied to the list price for the booking transaction.

---

## Technical Mapping

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Technical Column**: discount_pct

**Data Type**: Numeric

**Aggregation Type**: AVG

---

## Formula

This is a base measure captured directly from the booking transaction representing the discount rate applied to the list price.

**Discount Amount** = Unit List Price USD × Quantity Sold × Discount Percentage

**Net Price** = Unit List Price USD × (1 - Discount Percentage)

---

## Aggregation

**Default Aggregation**: AVG

**Valid Aggregations**:
- AVG: Average discount percentage across transactions
- MIN: Minimum discount percentage
- MAX: Maximum discount percentage
- MEDIAN: Median discount percentage

---

## Related Entities

- [Booking Transaction](../entities/booking-transaction.md): Source entity for this measure
- [Customer](../entities/customer.md): Analyze discount by customer attributes
- [Product](../entities/product.md): Analyze discount by product attributes
- [Partner](../entities/partner.md): Analyze discount by partner attributes
- [Geography](../entities/geography.md): Analyze discount by geographic attributes
- [Sales Representative](../entities/sales-representative.md): Analyze discount by sales representative
- [Contract](../entities/contract.md): Analyze discount by contract attributes
- [Date](../entities/date.md): Analyze discount trends over time

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. Discount Percentage represents the rate applied to list price
2. Discount is expressed as a decimal (e.g., 0.15 = 15% discount)
3. Discount reduces the list price to calculate booking amount
4. Average aggregation is most meaningful for discount percentage
5. Discount percentage varies by customer, product, partner, and deal size

---

## Usage Examples

**Discount Analysis**:
- Calculate average discount rate by customer segment
- Analyze discount trends over time

**Pricing Strategy**:
- Compare discount rates across product families
- Evaluate discount levels by partner type

**Margin Analysis**:
- Measure discount impact on revenue
- Identify high-discount transactions

**Discount by Dimension**:
- Average discount by customer tier
- Average discount by sales region
- Average discount by product family
- Average discount by partner type

---

## Related Measures

- [Unit List Price USD](unit-list-price-usd.md): Base price before discount
- [Booking Amount USD](booking-amount-usd.md): Revenue after discount
- [Quantity Sold](quantity-sold.md): Volume measure used in discount calculation

---

## Related Concepts

- [Discount Percentage](../glossary/discount-percentage.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Unit List Price USD](../glossary/unit-list-price-usd.md)

---

## Navigation

- [Back to Measures Index](index.md)
- [Back to Main Index](../index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [View Metrics](../metrics.md)
