---
title: Quantity Sold
type: measure
description: Number of units, licenses, or subscriptions included in the booking transaction
resource: measures
tags: [measure, quantity, volume, units, licenses]
timestamp: 2026-07-28T00:00:00Z
---

# Quantity Sold

## Business Definition

Number of units, licenses, or subscriptions included in the booking transaction.

---

## Technical Mapping

**Entity**: [Booking Transaction](../entities/booking-transaction.md)

**Technical Column**: quantity

**Data Type**: Integer

**Aggregation Type**: SUM

---

## Formula

This is a base measure captured directly from the booking transaction.

---

## Aggregation

**Default Aggregation**: SUM

**Valid Aggregations**:
- SUM: Total quantity sold across all transactions
- COUNT: Number of transactions with quantity
- AVG: Average quantity per transaction
- MIN: Minimum quantity in a transaction
- MAX: Maximum quantity in a transaction

---

## Related Entities

- [Booking Transaction](../entities/booking-transaction.md): Source entity for this measure
- [Customer](../entities/customer.md): Analyze quantity by customer attributes
- [Product](../entities/product.md): Analyze quantity by product attributes
- [Partner](../entities/partner.md): Analyze quantity by partner attributes
- [Geography](../entities/geography.md): Analyze quantity by geographic attributes
- [Sales Representative](../entities/sales-representative.md): Analyze quantity by sales representative
- [Contract](../entities/contract.md): Analyze quantity by contract attributes
- [Date](../entities/date.md): Analyze quantity trends over time

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. Quantity Sold represents the number of units, licenses, or subscriptions
2. Quantity is always a positive integer
3. Quantity can vary by product type (hardware units, software licenses, SaaS subscriptions)
4. Aggregation is typically SUM to calculate total volume
5. Quantity is used in pricing calculations along with unit price

---

## Usage Examples

**Total Volume Analysis**:
- Calculate total units/licenses/subscriptions sold
- Measure volume trends over time

**Product Volume Analysis**:
- Identify highest-volume products
- Compare volume by product family

**Customer Volume Analysis**:
- Measure purchase volume by customer segment
- Identify high-volume customers

**Geographic Volume Analysis**:
- Compare volume by sales region
- Analyze volume distribution by country

**Average Deal Size**:
- Calculate average quantity per transaction
- Compare average quantity by dimension

---

## Related Measures

- [Booking Amount USD](booking-amount-usd.md): Revenue measure related to quantity
- [Unit List Price USD](unit-list-price-usd.md): Pricing measure used with quantity
- [Discount Percentage](discount-percentage.md): Discount applied to quantity pricing

---

## Related Concepts

- [Quantity Sold](../glossary/quantity-sold.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Navigation

- [Back to Measures Index](index.md)
- [Back to Main Index](../index.md)
- [View Entity: Booking Transaction](../entities/booking-transaction.md)
- [View Metrics](../metrics.md)
