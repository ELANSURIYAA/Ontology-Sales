---
title: Measures Index
type: index
description: Navigation index for all business measures in the Quote to Booking semantic model
resource: measures
tags: [okf, measures, index, quote-to-booking]
timestamp: 2026-07-28T00:00:00Z
---

# Measures Index

## Overview

This index provides navigation to all business measures within the Quote to Booking semantic model. The model contains 6 core measures organized into volume, pricing, and revenue categories.

---

## Measure Catalog

### Volume Measures

#### [Quantity Sold](quantity-sold.md)
**Measure ID**: MEA001  
**Entity**: Booking Fact  
**Technical Column**: quantity  
**Aggregation**: Sum  
**Description**: Number of units, licenses, or subscriptions booked in the transaction

---

### Pricing Measures

#### [Unit List Price USD](unit-list-price-usd.md)
**Measure ID**: MEA002  
**Entity**: Booking Fact  
**Technical Column**: unit_list_price_usd  
**Aggregation**: Average  
**Description**: Standard list price per unit in U.S. dollars before discounts

---

#### [Discount Percentage](discount-percentage.md)
**Measure ID**: MEA003  
**Entity**: Booking Fact  
**Technical Column**: discount_pct  
**Aggregation**: Average  
**Description**: Discount applied to the list price for the booking line

---

### Revenue Measures

#### [Booking Amount USD](booking-amount-usd.md)
**Measure ID**: MEA004  
**Entity**: Booking Fact  
**Technical Column**: booking_amount_usd  
**Aggregation**: Sum  
**Description**: Total booked revenue amount in U.S. dollars for the transaction

---

#### [Annual Contract Value USD](annual-contract-value-usd.md)
**Measure ID**: MEA005  
**Entity**: Booking Fact  
**Technical Column**: acv_usd  
**Aggregation**: Sum  
**Description**: Annualized contract value in U.S. dollars used for recurring revenue analysis

---

#### [Total Contract Value USD](total-contract-value-usd.md)
**Measure ID**: MEA006  
**Entity**: Booking Fact  
**Technical Column**: tcv_usd  
**Aggregation**: Sum  
**Description**: Total contract value in U.S. dollars over the full contract term

---

## Measure Statistics

- **Total Measures**: 6
- **Volume Measures**: 1
- **Pricing Measures**: 2
- **Revenue Measures**: 3
- **Sum Aggregations**: 4
- **Average Aggregations**: 2

---

## Measure Categories

### By Business Purpose
- **Volume Tracking**: Quantity Sold
- **Pricing Analysis**: Unit List Price USD, Discount Percentage
- **Revenue Reporting**: Booking Amount USD, Annual Contract Value USD, Total Contract Value USD

### By Aggregation Type
- **Additive (Sum)**: Quantity Sold, Booking Amount USD, Annual Contract Value USD, Total Contract Value USD
- **Semi-Additive (Average)**: Unit List Price USD, Discount Percentage

---

## Navigation

- [Back to Bundle Index](../index.md)
- [Semantic Summary](../semantic_summary.md)
- [Metrics Catalog](../metrics.md)
- [Domains Index](../domains/index.md)
- [Entities Index](../entities/index.md)
- [Relationships Index](../relationships/index.md)
- [Glossary Index](../glossary/index.md)
