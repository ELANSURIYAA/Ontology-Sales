---
title: Unit List Price USD
type: measure
description: Standard list price per unit in U.S. dollars before discounts are applied
resource: measures
tags: [measure, price, pricing, list-price, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Unit List Price USD

## Business Definition

Standard list price per unit in U.S. dollars before discounts are applied.

---

## Technical Mapping

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Technical Column**: unit_list_price_usd

**Data Type**: Numeric

**Aggregation Type**: SUM

---

## Formula

This is a base measure captured directly from the booking transaction representing the standard list price before any discounts.

---

## Aggregation

**Default Aggregation**: SUM

**Valid Aggregations**:
- SUM: Total list price value across all transactions
- AVG: Average list price per unit
- MIN: Minimum list price
- MAX: Maximum list price

---

## Related Entities

- [Booking Transaction](../entities/booking-transaction.md): Source entity for this measure
- [Customer](../entities/customer.md): Analyze list price by customer attributes
- [Product](../entities/product.md): Analyze list price by product attributes
- [Partner](../entities/partner.md): Analyze list price by partner attributes
- [Geography](../entities/geography.md): Analyze list price by geographic attributes
- [Sales Representative](../entities/sales-representative.md): Analyze list price by sales representative
- [Contract](../entities/contract.md): Analyze list price by contract attributes
- [Date](../entities/date.md): Analyze list price trends over time

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. Unit List Price USD represents the standard list price before discounts
2. All prices are recorded in U.S. dollars
3. List price is the baseline for discount calculations
4. List price does not include any promotional or negotiated discounts
5. Used in conjunction with Quantity Sold and Discount Percentage to calculate Booking Amount

---

## Usage Examples

**Pricing Analysis**:
- Calculate average list price by product
- Analyze list price trends over time

**Product Pricing**:
- Compare list prices across product families
- Identify pricing tiers by product

**Discount Analysis**:
- Calculate discount amounts from list price
- Measure price realization (actual vs. list)

**Price Realization Formula**:
- Price Realization = Booking Amount USD / (Unit List Price USD × Quantity Sold)

---

## Related Measures

- [Booking Amount USD](booking-amount-usd.md): Actual revenue after discounts
- [Discount Percentage](discount-percentage.md): Discount applied to list price
- [Quantity Sold](quantity-sold.md): Volume measure used with price

---

## Related Concepts

- [Unit List Price USD](../glossary/unit-list-price-usd.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Discount Percentage](../glossary/discount-percentage.md)

---

## Navigation

- [Back to Measures Index](index.md)
- [Back to Main Index](../index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [View Metrics](../metrics.md)
