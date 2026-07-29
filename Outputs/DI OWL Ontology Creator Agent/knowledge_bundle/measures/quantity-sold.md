---
title: Quantity Sold
type: measure
description: Number of units, licenses, or subscriptions included in the booking transaction
resource: measures
tags: [measure, quantity, volume, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Quantity Sold

## Business Definition

Quantity Sold represents the number of units, licenses, or subscriptions included in the booking transaction. This measure tracks the volume of products or services sold and is fundamental for volume-based analysis, capacity planning, and sales performance measurement.

---

## Technical Mapping

**Measure ID**: MEA001  
**Technical Column**: quantity  
**Source Table**: QuoteToBooking.fact_bookings  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Data Type**: Integer

---

## Aggregation

**Aggregation Type**: SUM  
**Description**: Total quantity is calculated by summing individual transaction quantities across selected dimensions

---

## Formula

```
Total Quantity Sold = SUM(quantity)
```

---

## Business Rules

1. Quantity must be a positive integer
2. Quantity cannot be null for valid booking transactions
3. Quantity represents discrete units (licenses, subscriptions, devices)
4. Fractional quantities are not supported
5. Zero quantity bookings are invalid

---

## Analytical Usage

### Volume Analysis
- Track total units sold over time
- Compare volume across products and product families
- Analyze volume trends and patterns

### Sales Performance
- Measure sales representative productivity by volume
- Track team and territory volume performance
- Compare volume across customer segments

### Capacity Planning
- Forecast future volume requirements
- Plan inventory and resource allocation
- Identify volume growth opportunities

### Product Adoption
- Track product adoption rates
- Measure license deployment
- Analyze subscription volume trends

---

## Related Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Source entity containing quantity data
- **[Product](../entities/product.md)** - Products sold in quantities
- **[Customer](../entities/customer.md)** - Customers purchasing quantities
- **[Sales Representative](../entities/sales-representative.md)** - Representatives selling volumes

---

## Related Measures

- **[Booking Amount USD](./booking-amount-usd.md)** - Revenue derived from quantity sold
- **[Unit List Price USD](./unit-list-price-usd.md)** - Price per unit of quantity
- **[Discount Percentage](./discount-percentage.md)** - Discounts applied to quantity purchases

---

## Dimensional Analysis

Quantity Sold can be analyzed across:

- **[Date](../entities/date.md)** - Volume trends over time
- **[Product](../entities/product.md)** - Volume by product and family
- **[Customer](../entities/customer.md)** - Volume by customer segment
- **[Geography](../entities/geography.md)** - Volume by region and country
- **[Partner](../entities/partner.md)** - Volume by channel partner
- **[Sales Representative](../entities/sales-representative.md)** - Volume by sales rep
- **[Contract](../entities/contract.md)** - Volume by contract type

---

## Key Performance Indicators

- **Total Units Sold** - Sum of all quantities
- **Average Deal Size (Units)** - Average quantity per transaction
- **Volume Growth Rate** - Period-over-period quantity change
- **Volume per Customer** - Average quantity per customer
- **Volume per Representative** - Average quantity per sales rep

---

## Semantic Links

- [Measure Index](./index.md)
- [Metrics Overview](../metrics.md)
- [Booking Transaction Entity](../entities/booking-transaction.md)
- [Main Index](../index.md)

---

## Metadata

**Measure ID**: MEA001  
**Entity ID**: ENT008  
**Technical Column**: quantity  
**Data Type**: Integer  
**Aggregation**: SUM  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
