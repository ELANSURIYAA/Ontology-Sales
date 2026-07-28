---
title: Discount Percentage
type: measure
description: Percentage discount applied to the list price for the booking transaction
resource: measures
tags: [measure, pricing, discount, percentage, pricing-strategy]
timestamp: 2026-07-28T00:00:00Z
---

# Discount Percentage

## Business Definition

Percentage discount applied to the list price for the booking transaction. This measure tracks pricing concessions and supports analysis of discount strategies, pricing discipline, and margin management across customers, partners, and products.

---

## Measure Details

**Measure ID**: MEA003  
**Measure Type**: Pricing Metric  
**Aggregation Type**: AVG (Average)  
**Unit of Measure**: Percentage (%)

---

## Technical Mapping

**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Source Table**: QuoteToBooking.fact_bookings  
**Source Column**: discount_pct  
**Data Type**: numeric

---

## Formula

```
Discount Percentage = AVG(discount_pct)
```

Use AVERAGE aggregation to calculate mean discount percentage across transactions.

---

## Related Entities

### Source Entity
- [Booking Transaction](../entities/booking-transaction.md) - Fact table containing discount percentage values

### Analysis Dimensions
- [Customer](../entities/customer.md) - Analyze discounts by customer segment and account tier
- [Partner](../entities/partner.md) - Compare discounts by partner type and tier
- [Product](../entities/product.md) - Evaluate discounts by product family and offer type
- [Sales Representative](../entities/sales-representative.md) - Monitor discount levels by sales rep and team
- [Geography](../entities/geography.md) - Compare discount practices across regions
- [Date](../entities/date.md) - Track discount trends over time

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Aggregation**: Always use AVG (average) aggregation for discount percentage
2. **Range**: Discount percentage should be between 0 and 100
3. **Interpretation**: Higher percentages indicate larger discounts from list price
4. **Pricing Discipline**: Monitor to ensure discounts align with pricing policies
5. **Margin Impact**: Higher discounts reduce gross margins

---

## Usage Examples

### Average Discount by Customer Segment
Analyze average discount percentage by customer segment to assess pricing strategies for different customer types.

### Discount by Partner Type
Compare average discounts across partner types to evaluate channel pricing discipline.

### Sales Rep Discount Analysis
Monitor average discount percentage by sales representative to ensure pricing policy compliance.

### Discount Trend Analysis
Track average discount percentage over time to identify pricing pressure or policy changes.

---

## Related Measures

### Complementary Measures
- [Unit List Price USD](unit-list-price-usd.md) - Base price before discount
- [Booking Amount USD](booking-amount-usd.md) - Revenue after discount application
- [Quantity Sold](quantity-sold.md) - Volume sold at discounted prices

### Calculated Metrics
- **Discount Amount** = (Unit List Price USD × Quantity Sold) × (Discount Percentage / 100)
- **Net Price** = Unit List Price USD × (1 - Discount Percentage / 100)
- **Price Realization** = 100% - Discount Percentage

---

## Related Glossary Terms

- [Discount Percentage](../glossary/discount-percentage.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Analysis Guidelines

### Best Practices
- Use AVG aggregation (never SUM)
- Monitor by customer segment to ensure consistent pricing
- Track by partner to maintain channel pricing discipline
- Compare across sales representatives to identify outliers
- Analyze trends to detect pricing pressure

### Common Analysis Patterns
- Average discount by customer segment and account tier
- Discount comparison by partner type and tier
- Sales representative discount compliance
- Discount trends by fiscal period
- Product-level discount analysis

### Warning Indicators
- Discount percentages exceeding policy thresholds
- Increasing discount trends over time
- High variance in discounts across similar customers
- Unusual discount patterns by sales representative

---

## Navigation

- [View Measures Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [View Related Measures](index.md#pricing-measures)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Measure ID**: MEA003  
**Category**: Pricing Metric  
**Source Entity**: Booking Transaction  
**Aggregation**: AVG  
**Last Updated**: 2026-07-28T00:00:00Z
