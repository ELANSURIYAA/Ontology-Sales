---
title: Booking Amount USD
type: measure
description: Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments
resource: measures
tags: [measure, revenue, booking, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Amount USD

## Business Definition

Booking Amount USD represents the total booked revenue amount for the transaction in U.S. dollars after pricing adjustments. This is the primary revenue measure for sales performance tracking, quota attainment, and financial reporting. It reflects the actual revenue value after applying discounts to the list price.

---

## Technical Mapping

**Measure ID**: MEA004  
**Technical Column**: booking_amount_usd  
**Source Table**: QuoteToBooking.fact_bookings  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Data Type**: Numeric

---

## Aggregation

**Aggregation Type**: SUM  
**Description**: Total bookings are calculated by summing individual booking amounts across selected dimensions

---

## Formula

```
Booking Amount = Quantity × Unit List Price × (1 - Discount Percentage / 100)
Total Bookings = SUM(booking_amount_usd)
```

---

## Business Rules

1. Booking Amount must be non-negative
2. Booking Amount is expressed in U.S. dollars (USD)
3. Booking Amount reflects net revenue after discounts
4. Booking Amount is recognized at time of booking
5. Zero booking amounts may indicate promotional transactions

---

## Analytical Usage

### Revenue Reporting
- Track total bookings by period (daily, monthly, quarterly, yearly)
- Monitor revenue performance against targets and quotas
- Report financial results to stakeholders

### Sales Performance
- Measure sales representative and team performance
- Track quota attainment and achievement rates
- Compare performance across territories and segments

### Trend Analysis
- Analyze booking trends and growth rates
- Identify seasonal patterns and cycles
- Forecast future revenue based on historical trends

### Segmentation Analysis
- Compare revenue across customer segments
- Analyze product portfolio contribution
- Evaluate channel and partner performance

---

## Related Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Source entity containing booking amounts
- **[Customer](../entities/customer.md)** - Customer revenue contribution
- **[Product](../entities/product.md)** - Product revenue performance
- **[Sales Representative](../entities/sales-representative.md)** - Sales rep revenue credit
- **[Geography](../entities/geography.md)** - Regional revenue distribution
- **[Partner](../entities/partner.md)** - Channel revenue contribution

---

## Related Measures

- **[Quantity Sold](./quantity-sold.md)** - Volume component of booking amount
- **[Unit List Price USD](./unit-list-price-usd.md)** - Base price component
- **[Discount Percentage](./discount-percentage.md)** - Discount applied to calculate booking amount
- **[Annual Contract Value USD](./annual-contract-value-usd.md)** - Annualized booking value
- **[Total Contract Value USD](./total-contract-value-usd.md)** - Full contract value

---

## Calculation Relationships

```
Booking Amount = Quantity × Unit List Price × (1 - Discount Percentage / 100)
Effective Price = Booking Amount / Quantity
Discount Amount = (Quantity × Unit List Price) - Booking Amount
Price Realization = Booking Amount / (Quantity × Unit List Price) × 100
```

---

## Dimensional Analysis

Booking Amount USD can be analyzed across:

- **[Date](../entities/date.md)** - Revenue trends over time
- **[Product](../entities/product.md)** - Product portfolio revenue
- **[Customer](../entities/customer.md)** - Customer segment revenue
- **[Geography](../entities/geography.md)** - Regional revenue performance
- **[Partner](../entities/partner.md)** - Channel revenue contribution
- **[Sales Representative](../entities/sales-representative.md)** - Sales rep performance
- **[Contract](../entities/contract.md)** - Contract type revenue

---

## Key Performance Indicators

- **Total Bookings** - Sum of all booking amounts
- **Average Deal Size** - Average booking amount per transaction
- **Booking Growth Rate** - Period-over-period booking change
- **Bookings per Customer** - Average bookings per customer
- **Bookings per Representative** - Average bookings per sales rep
- **Quota Attainment** - Actual bookings / Target bookings × 100

---

## Business Context

Booking Amount USD is the most critical measure in the sales bookings model as it:
- Drives sales compensation and commissions
- Determines quota achievement
- Supports financial planning and forecasting
- Enables performance management
- Provides basis for revenue recognition

---

## Semantic Links

- [Measure Index](./index.md)
- [Metrics Overview](../metrics.md)
- [Booking Transaction Entity](../entities/booking-transaction.md)
- [Main Index](../index.md)

---

## Metadata

**Measure ID**: MEA004  
**Entity ID**: ENT008  
**Technical Column**: booking_amount_usd  
**Data Type**: Numeric  
**Aggregation**: SUM  
**Currency**: USD  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
