---
title: Quantity Sold
type: measure
description: Number of units, licenses, or subscriptions included in the booking transaction
resource: measures
tags: [measure, volume, quantity, units, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Quantity Sold

## Business Definition

Number of units, licenses, or subscriptions included in the booking transaction. This measure tracks the volume of products sold and supports analysis of sales adoption, market penetration, and product usage patterns.

---

## Measure Details

**Measure ID**: MEA001  
**Measure Type**: Volume Metric  
**Aggregation Type**: SUM  
**Unit of Measure**: Units/Licenses/Subscriptions

---

## Technical Mapping

**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Source Table**: QuoteToBooking.fact_bookings  
**Source Column**: quantity  
**Data Type**: integer

---

## Formula

```
Quantity Sold = SUM(quantity)
```

No calculation required - direct aggregation of quantity values from booking transactions.

---

## Related Entities

### Source Entity
- [Booking Transaction](../entities/booking-transaction.md) - Fact table containing quantity values

### Analysis Dimensions
- [Product](../entities/product.md) - Analyze quantities by product, family, and technology domain
- [Customer](../entities/customer.md) - Analyze quantities by customer segment and industry
- [Date](../entities/date.md) - Track quantity trends over time
- [Geography](../entities/geography.md) - Compare quantities across regions
- [Partner](../entities/partner.md) - Evaluate partner volume performance

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Aggregation**: Always use SUM aggregation for quantity sold
2. **Granularity**: Quantity is recorded at the booking transaction level
3. **Unit Type**: Represents units, licenses, or subscriptions depending on product type
4. **Non-Negative**: Quantity values should be positive integers
5. **Analysis Context**: Meaningful when analyzed by product, customer, or time dimensions

---

## Usage Examples

### Total Quantity by Product Family
Analyze total units sold by product family to understand volume distribution across the portfolio.

### Quantity Trend Analysis
Track quantity sold over fiscal quarters to identify growth patterns and seasonal trends.

### Customer Volume Analysis
Compare quantities purchased by customer segment to assess adoption rates.

### Product Adoption
Identify products with highest quantities sold to understand market acceptance.

---

## Related Measures

### Complementary Measures
- [Booking Amount USD](booking-amount-usd.md) - Revenue associated with quantities sold
- [Unit List Price USD](unit-list-price-usd.md) - Pricing per unit
- [Discount Percentage](discount-percentage.md) - Discount levels affecting unit sales

### Calculated Metrics
- **Average Unit Price** = Booking Amount USD / Quantity Sold
- **Average Quantity per Transaction** = SUM(Quantity Sold) / COUNT(Booking ID)

---

## Related Glossary Terms

- [Quantity Sold](../glossary/quantity-sold.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Analysis Guidelines

### Best Practices
- Use SUM aggregation across all dimensions
- Analyze by product to understand volume drivers
- Compare with revenue measures to assess pricing effectiveness
- Track trends over time to identify growth patterns

### Common Analysis Patterns
- Volume by product family and technology domain
- Quantity trends by fiscal period
- Customer adoption by segment
- Geographic volume distribution

---

## Navigation

- [View Measures Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [View Related Measures](index.md#volume-measures)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Measure ID**: MEA001  
**Category**: Volume Metric  
**Source Entity**: Booking Transaction  
**Aggregation**: SUM  
**Last Updated**: 2026-07-28T00:00:00Z
