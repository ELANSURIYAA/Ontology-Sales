---
title: Unit List Price USD
type: measure
description: Standard list price per unit in U.S. dollars before discounts are applied
resource: measures
tags: [measure, price, pricing, list-price]
timestamp: 2026-07-28T00:00:00Z
---

# Unit List Price USD

## Business Definition

Unit List Price USD represents the standard list price per unit in U.S. dollars before discounts are applied. This measure establishes the baseline pricing for products and services and is used for pricing strategy analysis, discount calculation, and revenue potential assessment.

---

## Technical Mapping

**Measure ID**: MEA002  
**Technical Column**: unit_list_price_usd  
**Source Table**: QuoteToBooking.fact_bookings  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Data Type**: Numeric

---

## Aggregation

**Aggregation Type**: SUM  
**Description**: Total list price value is calculated by summing unit list prices across selected dimensions

---

## Formula

```
Total Unit List Price = SUM(unit_list_price_usd)
Average Unit List Price = AVG(unit_list_price_usd)
```

---

## Business Rules

1. Unit List Price must be non-negative
2. Unit List Price is expressed in U.S. dollars (USD)
3. Unit List Price represents the standard published price before discounts
4. Unit List Price does not include promotional pricing or discounts
5. Zero list price may indicate promotional or free offerings

---

## Analytical Usage

### Pricing Strategy
- Analyze standard pricing across product portfolio
- Compare list prices by product family and technology domain
- Track list price changes and trends over time

### Revenue Potential
- Calculate maximum revenue potential (List Price × Quantity)
- Assess pricing power and market positioning
- Evaluate price positioning by customer segment

### Discount Analysis
- Calculate discount amounts (List Price - Net Price)
- Measure discount impact on revenue
- Compare actual pricing to list pricing

### Competitive Analysis
- Benchmark list prices against market standards
- Analyze price positioning by geography
- Track competitive pricing dynamics

---

## Related Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Source entity containing price data
- **[Product](../entities/product.md)** - Products with list prices
- **[Customer](../entities/customer.md)** - Customers receiving list price quotes
- **[Partner](../entities/partner.md)** - Partners selling at list price

---

## Related Measures

- **[Discount Percentage](./discount-percentage.md)** - Discount applied to list price
- **[Booking Amount USD](./booking-amount-usd.md)** - Net revenue after discounts
- **[Quantity Sold](./quantity-sold.md)** - Volume sold at list price

---

## Calculation Relationships

```
Booking Amount = Quantity × Unit List Price × (1 - Discount Percentage / 100)
Discount Amount = Quantity × Unit List Price × (Discount Percentage / 100)
Revenue Potential = Quantity × Unit List Price
```

---

## Dimensional Analysis

Unit List Price USD can be analyzed across:

- **[Date](../entities/date.md)** - Price trends over time
- **[Product](../entities/product.md)** - Pricing by product and family
- **[Customer](../entities/customer.md)** - Pricing by customer segment
- **[Geography](../entities/geography.md)** - Regional pricing patterns
- **[Partner](../entities/partner.md)** - Channel pricing strategies
- **[Contract](../entities/contract.md)** - Pricing by contract type

---

## Key Performance Indicators

- **Average List Price** - Mean list price across transactions
- **List Price Range** - Min and max list prices
- **Price Realization Rate** - (Booking Amount / List Price Value) × 100
- **List Price Growth** - Period-over-period list price change

---

## Semantic Links

- [Measure Index](./index.md)
- [Metrics Overview](../metrics.md)
- [Booking Transaction Entity](../entities/booking-transaction.md)
- [Main Index](../index.md)

---

## Metadata

**Measure ID**: MEA002  
**Entity ID**: ENT008  
**Technical Column**: unit_list_price_usd  
**Data Type**: Numeric  
**Aggregation**: SUM  
**Currency**: USD  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
