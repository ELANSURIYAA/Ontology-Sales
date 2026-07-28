---
title: Booking Amount USD
type: measure
description: Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments
resource: measures
tags: [measure, revenue, booking, usd, financial]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Amount USD

## Business Definition

Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments. This is the primary revenue metric for sales performance analysis and financial reporting, representing the actual revenue recognized from booking transactions.

---

## Measure Details

**Measure ID**: MEA004  
**Measure Type**: Revenue Metric  
**Aggregation Type**: SUM  
**Unit of Measure**: USD (U.S. Dollars)

---

## Technical Mapping

**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Source Table**: QuoteToBooking.fact_bookings  
**Source Column**: booking_amount_usd  
**Data Type**: numeric

---

## Formula

```
Booking Amount USD = SUM(booking_amount_usd)
```

Alternatively calculated as:
```
Booking Amount USD = Quantity × Unit List Price USD × (1 - Discount Percentage / 100)
```

---

## Related Entities

### Source Entity
- [Booking Transaction](../entities/booking-transaction.md) - Fact table containing booking amount values

### Analysis Dimensions
- [Customer](../entities/customer.md) - Analyze revenue by customer segment, industry, and account tier
- [Product](../entities/product.md) - Evaluate revenue by product family, technology domain, and offer type
- [Geography](../entities/geography.md) - Compare revenue across regions, theaters, and countries
- [Date](../entities/date.md) - Track revenue trends over fiscal and calendar periods
- [Partner](../entities/partner.md) - Assess partner contribution to revenue
- [Sales Representative](../entities/sales-representative.md) - Measure sales team performance
- [Contract](../entities/contract.md) - Analyze revenue by contract characteristics

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Aggregation**: Always use SUM aggregation for booking amount
2. **Currency**: All values are in U.S. dollars (USD)
3. **Post-Discount**: Represents revenue after discount application
4. **Primary Metric**: This is the primary revenue measure for sales performance
5. **Non-Negative**: Booking amounts should be positive values
6. **Completeness**: Should be populated for all booking transactions

---

## Usage Examples

### Total Revenue by Fiscal Quarter
Calculate total booking amount by fiscal quarter to support financial reporting and performance tracking.

### Revenue by Customer Segment
Analyze booking amount by customer segment to understand revenue distribution and segment performance.

### Product Portfolio Revenue
Evaluate booking amount by product family to assess portfolio performance and revenue drivers.

### Geographic Revenue Analysis
Compare booking amounts across sales regions to identify high-performing markets.

### Sales Team Performance
Measure booking amount by sales representative and team to track quota attainment.

---

## Related Measures

### Complementary Measures
- [Quantity Sold](quantity-sold.md) - Volume associated with revenue
- [Unit List Price USD](unit-list-price-usd.md) - Base pricing before discounts
- [Discount Percentage](discount-percentage.md) - Discount impact on revenue
- [Annual Contract Value USD](annual-contract-value-usd.md) - Annualized contract revenue
- [Total Contract Value USD](total-contract-value-usd.md) - Total contract revenue

### Calculated Metrics
- **Average Deal Size** = SUM(Booking Amount USD) / COUNT(Booking ID)
- **Revenue per Customer** = SUM(Booking Amount USD) / COUNT(DISTINCT Customer Key)
- **Revenue per Sales Rep** = SUM(Booking Amount USD) / COUNT(DISTINCT Sales Rep Key)
- **Average Unit Price** = SUM(Booking Amount USD) / SUM(Quantity Sold)

---

## Related Glossary Terms

- [Booking Amount USD](../glossary/booking-amount-usd.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Analysis Guidelines

### Best Practices
- Use SUM aggregation across all dimensions
- Primary metric for sales performance dashboards
- Compare across time periods for growth analysis
- Analyze by multiple dimensions for comprehensive insights
- Use for quota tracking and sales forecasting

### Common Analysis Patterns
- Total bookings by fiscal quarter and year
- Revenue by customer segment and industry
- Product family and technology domain revenue
- Geographic revenue distribution
- Partner contribution analysis
- Sales team performance tracking
- New vs renewal revenue comparison

### Key Performance Indicators
- **Total Bookings**: SUM(Booking Amount USD)
- **Booking Growth**: (Current Period - Prior Period) / Prior Period
- **Average Deal Size**: Booking Amount / Transaction Count
- **Revenue Concentration**: Top 10 Customers / Total Bookings

---

## Navigation

- [View Measures Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [View Related Measures](index.md#revenue-measures)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Measure ID**: MEA004  
**Category**: Revenue Metric  
**Source Entity**: Booking Transaction  
**Aggregation**: SUM  
**Last Updated**: 2026-07-28T00:00:00Z
