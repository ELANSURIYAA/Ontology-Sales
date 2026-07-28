---
title: Measures Index
type: index
description: Navigation index for business measures
resource: measures
tags: [measures, index, metrics, kpi]
timestamp: 2026-07-28T00:00:00Z
---

# Measures Index

This index provides navigation to all business measure documents in the knowledge bundle.

---

## Measure Overview

The knowledge bundle contains **6** business measures, all associated with the Booking Transaction fact entity.

---

## Revenue Measures

### [Booking Amount USD](booking-amount-usd.md)

**Definition**: Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments

**Aggregation**: SUM  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Technical Column**: booking_amount_usd

---

### [Annual Contract Value USD](annual-contract-value-usd.md)

**Definition**: Annualized value of the contract associated with the booking in U.S. dollars

**Aggregation**: SUM  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Technical Column**: acv_usd

---

### [Total Contract Value USD](total-contract-value-usd.md)

**Definition**: Total value of the full contract associated with the booking in U.S. dollars

**Aggregation**: SUM  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Technical Column**: tcv_usd

---

## Volume Measures

### [Quantity Sold](quantity-sold.md)

**Definition**: Number of units, licenses, or subscriptions included in the booking transaction

**Aggregation**: SUM  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Technical Column**: quantity

---

## Pricing Measures

### [Unit List Price USD](unit-list-price-usd.md)

**Definition**: Standard list price per unit in U.S. dollars before discounts are applied

**Aggregation**: SUM  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Technical Column**: unit_list_price_usd

---

### [Discount Percentage](discount-percentage.md)

**Definition**: Percentage discount applied to the list price for the booking transaction

**Aggregation**: AVG  
**Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Technical Column**: discount_pct

---

## Measure Categories

**Revenue Metrics**:
- Booking Amount USD
- Annual Contract Value USD
- Total Contract Value USD

**Volume Metrics**:
- Quantity Sold

**Pricing Metrics**:
- Unit List Price USD
- Discount Percentage

---

## Analysis Dimensions

All measures can be analyzed across:
- [Customer](../entities/customer.md)
- [Product](../entities/product.md)
- [Partner](../entities/partner.md)
- [Geography](../entities/geography.md)
- [Sales Representative](../entities/sales-representative.md)
- [Contract](../entities/contract.md)
- [Date](../entities/date.md)

---

## Navigation

- [Back to Index](../index.md)
- [Semantic Summary](../semantic_summary.md)
- [View Metrics](../metrics.md)
- [View Domains](../domains/index.md)
- [View Entities](../entities/index.md)
- [View Relationships](../relationships/index.md)
- [View Glossary](../glossary/index.md)
