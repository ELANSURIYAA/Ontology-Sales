---
title: Bookings Domain
type: domain
description: Individual completed sales booking transactions with financial measures, quantities, renewal status, and dimensional links
resource: domains
tags: [bookings, transactions, sales, fact, revenue]
timestamp: 2024-01-15T00:00:00Z
---

# Bookings Domain

## Business Definition

The Bookings domain captures individual completed sales booking transactions and their associated financial measures, quantities, renewal status, and links to related business dimensions. This domain represents the core fact table in the sales bookings and revenue analytics model.

---

## Business Purpose

The Bookings domain serves as the atomic unit of analysis for sales performance, revenue recognition, and booking analytics. It enables analysis of:

- Sales transaction volumes and values
- Revenue performance across dimensions
- Renewal vs net new business mix
- Discount and pricing effectiveness
- Contract value analysis (ACV/TCV)
- Order and line-level detail

---

## Domain Type

**Fact Domain** - Transactional grain at the individual booking transaction level

---

## Related Entities

- [Booking Transaction](../entities/bookings.md)

---

## Related Measures

### Volume Measures
- [Booking Count](../measures/booking-count.md)
- [Distinct Order Count](../measures/distinct-order-count.md)
- [Total Quantity](../measures/total-quantity.md)

### Revenue Measures
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

### Average Measures
- [Average Discount Percentage](../measures/average-discount-pct.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)
- [Average Booking Value USD](../measures/average-booking-value-usd.md)

---

## Related Relationships

- [Bookings to Contracts](../relationships/bookings-to-contracts.md)
- [Bookings to Customers](../relationships/bookings-to-customers.md)
- [Bookings to Dates](../relationships/bookings-to-dates.md)
- [Bookings to Geographies](../relationships/bookings-to-geographies.md)
- [Bookings to Partners](../relationships/bookings-to-partners.md)
- [Bookings to Products](../relationships/bookings-to-products.md)
- [Bookings to Sales Representatives](../relationships/bookings-to-sales-representatives.md)

---

## Key Concepts

### Booking Transaction
A completed sales booking event representing a customer commitment to purchase products or services.

### Booking Amount
The total revenue value of the booking after applying discounts and pricing adjustments.

### Annual Contract Value (ACV)
The annualized value of the booking, used for subscription and recurring revenue analysis.

### Total Contract Value (TCV)
The full contract value over the entire term, used for multi-year deal analysis.

### Renewal Flag
Indicator distinguishing renewal transactions from net new business.

---

## Semantic Links

### Dimensional Context
- [Customers Domain](customers.md) - Who purchased
- [Products Domain](products.md) - What was purchased
- [Partners Domain](partners.md) - Through which channel
- [Geographies Domain](geographies.md) - Where the sale occurred
- [Sales Representatives Domain](sales-representatives.md) - Who sold it
- [Contracts Domain](contracts.md) - Under what terms
- [Dates Domain](dates.md) - When it was booked

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings  
**Primary Key**: booking_id  
**Grain**: One row per booking transaction

---

## Navigation

- [Return to Domains Index](index.md)
- [Return to Main Index](../index.md)
- [View Booking Transaction Entity](../entities/bookings.md)
