---
title: Annual Contract Value USD
type: measure
description: Annualized value of the contract associated with the booking in U.S. dollars
resource: measures
tags: [measure, revenue, acv, contract-value, recurring-revenue, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Annual Contract Value USD

## Business Definition

Annualized value of the contract associated with the booking in U.S. dollars. This measure represents the yearly recurring revenue from contracts and supports analysis of subscription performance, recurring revenue streams, and contract-based business models.

---

## Measure Details

**Measure ID**: MEA005  
**Measure Type**: Revenue Metric  
**Aggregation Type**: SUM  
**Unit of Measure**: USD (U.S. Dollars)

---

## Technical Mapping

**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Source Table**: QuoteToBooking.fact_bookings  
**Source Column**: acv_usd  
**Data Type**: numeric

---

## Formula

```
Annual Contract Value USD = SUM(acv_usd)
```

Alternatively calculated as:
```
Annual Contract Value USD = Total Contract Value USD / Contract Term Months × 12
```

---

## Related Entities

### Source Entity
- [Booking Transaction](../entities/booking-transaction.md) - Fact table containing ACV values

### Analysis Dimensions
- [Contract](../entities/contract.md) - Analyze ACV by contract type, term, and coverage level
- [Customer](../entities/customer.md) - Evaluate ACV by customer segment and account tier
- [Product](../entities/product.md) - Assess ACV by product family and offer type
- [Date](../entities/date.md) - Track ACV trends over time
- [Geography](../entities/geography.md) - Compare ACV across regions
- [Partner](../entities/partner.md) - Evaluate partner ACV contribution
- [Sales Representative](../entities/sales-representative.md) - Measure sales team ACV performance

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Aggregation**: Always use SUM aggregation for ACV
2. **Currency**: All values are in U.S. dollars (USD)
3. **Annualization**: Represents yearly recurring revenue from contracts
4. **Subscription Focus**: Particularly relevant for subscription and SaaS products
5. **Non-Negative**: ACV values should be positive
6. **Contract Relationship**: Derived from total contract value and contract term

---

## Usage Examples

### Total ACV by Product Family
Calculate total annual contract value by product family to assess recurring revenue by portfolio.

### ACV by Customer Segment
Analyze ACV by customer segment to understand recurring revenue distribution.

### ACV Growth Tracking
Track ACV trends over fiscal periods to measure recurring revenue growth.

### Contract Type ACV Analysis
Compare ACV across contract types to evaluate subscription model effectiveness.

### New vs Renewal ACV
Separate ACV by booking type to distinguish new recurring revenue from renewal revenue.

---

## Related Measures

### Complementary Measures
- [Total Contract Value USD](total-contract-value-usd.md) - Total contract value over full term
- [Booking Amount USD](booking-amount-usd.md) - Total booking revenue
- [Quantity Sold](quantity-sold.md) - Volume of subscriptions sold

### Calculated Metrics
- **Average ACV per Customer** = SUM(ACV USD) / COUNT(DISTINCT Customer Key)
- **ACV Growth Rate** = (Current Period ACV - Prior Period ACV) / Prior Period ACV
- **ACV per Sales Rep** = SUM(ACV USD) / COUNT(DISTINCT Sales Rep Key)
- **Contract Term** = Total Contract Value USD / Annual Contract Value USD

---

## Related Glossary Terms

- [Annual Contract Value USD](../glossary/annual-contract-value-usd.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Contract](../glossary/contract.md)

---

## Analysis Guidelines

### Best Practices
- Use SUM aggregation across all dimensions
- Focus on subscription and SaaS products
- Track ACV growth as a key recurring revenue metric
- Compare with TCV to understand contract duration
- Separate new ACV from renewal ACV for growth analysis

### Common Analysis Patterns
- Total ACV by fiscal quarter and year
- ACV by product family and offer type
- Customer segment ACV distribution
- New vs renewal ACV comparison
- ACV retention and churn analysis
- Geographic ACV performance

### Key Performance Indicators
- **Total ACV**: SUM(Annual Contract Value USD)
- **ACV Growth**: (Current Period ACV - Prior Period ACV) / Prior Period ACV
- **Average ACV**: SUM(ACV) / COUNT(Contracts)
- **ACV Retention Rate**: Renewal ACV / Prior Period ACV

---

## Navigation

- [View Measures Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [View Contract Entity](../entities/contract.md)
- [View Related Measures](index.md#revenue-measures)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Measure ID**: MEA005  
**Category**: Revenue Metric  
**Source Entity**: Booking Transaction  
**Aggregation**: SUM  
**Last Updated**: 2026-07-28T00:00:00Z
