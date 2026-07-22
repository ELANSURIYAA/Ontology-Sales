---
title: Metrics Overview
type: metrics_index
domain: Sales Bookings and Revenue Analytics
version: 1.0
status: generated
---

# Metrics Overview

## Measure Inventory

| Measure | Aggregation Type | Related Entity | Related Domain |
| --- | --- | --- | --- |
| [Quantity Sold](measures/quantity-sold.md) | Sum | [Booking Transaction](entities/booking-transaction.md) | [Sales Bookings and Revenue Analytics](domains/sales-bookings-and-revenue-analytics.md) |
| [Unit List Price USD](measures/unit-list-price-usd.md) | Average | [Booking Transaction](entities/booking-transaction.md) | [Sales Bookings and Revenue Analytics](domains/sales-bookings-and-revenue-analytics.md) |
| [Discount Percentage](measures/discount-percentage.md) | Average | [Booking Transaction](entities/booking-transaction.md) | [Sales Bookings and Revenue Analytics](domains/sales-bookings-and-revenue-analytics.md) |
| [Booking Amount USD](measures/booking-amount-usd.md) | Sum | [Booking Transaction](entities/booking-transaction.md) | [Sales Bookings and Revenue Analytics](domains/sales-bookings-and-revenue-analytics.md) |
| [Annual Contract Value USD](measures/annual-contract-value-usd.md) | Sum | [Booking Transaction](entities/booking-transaction.md) | [Sales Bookings and Revenue Analytics](domains/sales-bookings-and-revenue-analytics.md) |
| [Total Contract Value USD](measures/total-contract-value-usd.md) | Sum | [Booking Transaction](entities/booking-transaction.md) | [Sales Bookings and Revenue Analytics](domains/sales-bookings-and-revenue-analytics.md) |

## Observations

- Revenue-oriented measures are concentrated in the booking fact entity.
- Quantity is additive across transactions.
- Price and discount measures are modeled as average-oriented analytical measures.
- ACV and TCV support contract value analysis across time, product, customer, and partner dimensions.