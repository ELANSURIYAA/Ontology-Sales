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

Discount Percentage represents the percentage discount applied to the list price for the booking transaction. This measure quantifies pricing adjustments and is critical for margin analysis, pricing effectiveness evaluation, and competitive positioning assessment.

---

## Technical Mapping

**Measure ID**: MEA003  
**Technical Column**: discount_pct  
**Source Table**: QuoteToBooking.fact_bookings  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Data Type**: Numeric

---

## Aggregation

**Aggregation Type**: AVG  
**Description**: Average discount percentage is calculated across selected dimensions to understand typical discounting patterns

---

## Formula

```
Average Discount Percentage = AVG(discount_pct)
Weighted Average Discount = SUM(discount_pct × booking_amount_usd) / SUM(booking_amount_usd)
```

---

## Business Rules

1. Discount Percentage must be between 0 and 100
2. Zero discount indicates list price transaction
3. Negative discounts are not permitted
4. Discount Percentage is expressed as a whole number (e.g., 15 = 15%)
5. Discount applies to unit list price before calculating booking amount

---

## Analytical Usage

### Discount Analysis
- Track average discount rates across dimensions
- Identify high-discount transactions and patterns
- Monitor discount trends over time

### Margin Management
- Assess impact of discounting on margins
- Compare discount rates by customer segment and tier
- Evaluate discount effectiveness on deal closure

### Pricing Strategy
- Analyze discount patterns by product family
- Compare channel discount strategies
- Optimize discount policies and guidelines

### Competitive Positioning
- Benchmark discount rates against market standards
- Analyze geographic discount variations
- Track competitive pricing pressure

---

## Related Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Source entity containing discount data
- **[Product](../entities/product.md)** - Products with discount rates
- **[Customer](../entities/customer.md)** - Customer-specific discounting
- **[Partner](../entities/partner.md)** - Channel discount structures
- **[Sales Representative](../entities/sales-representative.md)** - Sales rep discount authority

---

## Related Measures

- **[Unit List Price USD](./unit-list-price-usd.md)** - Base price before discount
- **[Booking Amount USD](./booking-amount-usd.md)** - Net revenue after discount
- **[Quantity Sold](./quantity-sold.md)** - Volume impacted by discounting

---

## Calculation Relationships

```
Discount Amount = Quantity × Unit List Price × (Discount Percentage / 100)
Net Price = Unit List Price × (1 - Discount Percentage / 100)
Booking Amount = Quantity × Unit List Price × (1 - Discount Percentage / 100)
```

---

## Dimensional Analysis

Discount Percentage can be analyzed across:

- **[Date](../entities/date.md)** - Discount trends over time
- **[Product](../entities/product.md)** - Discounting by product
- **[Customer](../entities/customer.md)** - Customer segment discounting
- **[Geography](../entities/geography.md)** - Regional discount patterns
- **[Partner](../entities/partner.md)** - Channel discount strategies
- **[Sales Representative](../entities/sales-representative.md)** - Rep discount behavior
- **[Contract](../entities/contract.md)** - Contract-based discounting

---

## Key Performance Indicators

- **Average Discount Rate** - Mean discount percentage
- **Discount Range** - Min and max discount percentages
- **Zero Discount Rate** - Percentage of transactions at list price
- **High Discount Rate** - Percentage of transactions above threshold
- **Discount Impact** - Revenue loss due to discounting

---

## Business Thresholds

### Typical Discount Ranges
- **0-10%**: Standard discount range
- **10-20%**: Moderate discount range
- **20-30%**: High discount range
- **30%+**: Exceptional discount requiring approval

---

## Semantic Links

- [Measure Index](./index.md)
- [Metrics Overview](../metrics.md)
- [Booking Transaction Entity](../entities/booking-transaction.md)
- [Main Index](../index.md)

---

## Metadata

**Measure ID**: MEA003  
**Entity ID**: ENT008  
**Technical Column**: discount_pct  
**Data Type**: Numeric  
**Aggregation**: AVG  
**Unit**: Percentage  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
