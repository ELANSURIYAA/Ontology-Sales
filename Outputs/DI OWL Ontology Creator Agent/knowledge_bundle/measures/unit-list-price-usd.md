---
title: Unit List Price USD
type: measure
description: Standard list price per unit in U.S. dollars before discounts are applied
resource: measures
tags: [measure, pricing, list-price, usd, standard-price]
timestamp: 2026-07-28T00:00:00Z
---

# Unit List Price USD

## Business Definition

Standard list price per unit in U.S. dollars before discounts are applied. This measure represents the baseline pricing for products and supports analysis of pricing strategies, discount impacts, and price realization.

---

## Measure Details

**Measure ID**: MEA002  
**Measure Type**: Pricing Metric  
**Aggregation Type**: SUM  
**Unit of Measure**: USD (U.S. Dollars)

---

## Technical Mapping

**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Source Table**: QuoteToBooking.fact_bookings  
**Source Column**: unit_list_price_usd  
**Data Type**: numeric

---

## Formula

```
Unit List Price USD = SUM(unit_list_price_usd)
```

No calculation required - direct aggregation of unit list price values from booking transactions.

---

## Related Entities

### Source Entity
- [Booking Transaction](../entities/booking-transaction.md) - Fact table containing unit list price values

### Analysis Dimensions
- [Product](../entities/product.md) - Analyze list prices by product, family, and offer type
- [Date](../entities/date.md) - Track pricing changes over time
- [Customer](../entities/customer.md) - Compare list prices across customer segments
- [Geography](../entities/geography.md) - Evaluate pricing by region

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Aggregation**: Use SUM aggregation for total list price value
2. **Currency**: All values are in U.S. dollars (USD)
3. **Pre-Discount**: Represents pricing before discount application
4. **Standard Pricing**: Reflects published or standard list prices
5. **Non-Negative**: List price values should be positive

---

## Usage Examples

### Average List Price by Product
Calculate average unit list price by product to understand pricing positioning.

### Price Change Analysis
Track unit list price trends over time to identify pricing adjustments.

### Pricing Strategy Analysis
Compare list prices across product families and technology domains to evaluate pricing strategy.

### Price Realization
Compare unit list price with actual booking amount to calculate price realization and discount impact.

---

## Related Measures

### Complementary Measures
- [Discount Percentage](discount-percentage.md) - Discount applied to list price
- [Booking Amount USD](booking-amount-usd.md) - Actual revenue after discounts
- [Quantity Sold](quantity-sold.md) - Volume sold at list price

### Calculated Metrics
- **Price Realization** = Booking Amount USD / (Unit List Price USD × Quantity Sold)
- **Average Unit List Price** = SUM(Unit List Price USD) / SUM(Quantity Sold)
- **Discount Amount** = (Unit List Price USD × Quantity Sold) - Booking Amount USD

---

## Related Glossary Terms

- [Unit List Price USD](../glossary/unit-list-price-usd.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Analysis Guidelines

### Best Practices
- Use SUM aggregation for total list price value
- Calculate average list price by dividing by quantity for per-unit analysis
- Compare with booking amount to assess discount impact
- Track over time to monitor pricing strategy changes

### Common Analysis Patterns
- List price by product family and offer type
- Pricing trends by fiscal period
- Price positioning by technology domain
- List price vs actual price realization

---

## Navigation

- [View Measures Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [View Related Measures](index.md#pricing-measures)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Measure ID**: MEA002  
**Category**: Pricing Metric  
**Source Entity**: Booking Transaction  
**Aggregation**: SUM  
**Last Updated**: 2026-07-28T00:00:00Z
