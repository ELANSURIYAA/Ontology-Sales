---
title: Annual Contract Value USD
type: measure
description: Annualized value of the contract associated with the booking in U.S. dollars
resource: measures
tags: [measure, acv, contract, revenue, recurring]
timestamp: 2026-07-28T00:00:00Z
---

# Annual Contract Value USD

## Business Definition

Annual Contract Value (ACV) USD represents the annualized value of the contract associated with the booking in U.S. dollars. This measure normalizes contract values to an annual basis, enabling comparison of contracts with different terms and supporting recurring revenue analysis for subscription-based business models.

---

## Technical Mapping

**Measure ID**: MEA005  
**Technical Column**: acv_usd  
**Source Table**: QuoteToBooking.fact_bookings  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Data Type**: Numeric

---

## Aggregation

**Aggregation Type**: SUM  
**Description**: Total ACV is calculated by summing individual annual contract values across selected dimensions

---

## Formula

```
Annual Contract Value (ACV) = Total Contract Value (TCV) / Contract Term (Years)
Total ACV = SUM(acv_usd)
```

---

## Business Rules

1. ACV must be non-negative
2. ACV is expressed in U.S. dollars (USD)
3. ACV represents annualized recurring revenue
4. ACV normalizes multi-year contracts to annual basis
5. ACV is calculated by dividing TCV by contract term in years

---

## Analytical Usage

### Recurring Revenue Analysis
- Track annual recurring revenue (ARR) trends
- Monitor subscription revenue growth
- Forecast future recurring revenue streams

### Contract Comparison
- Compare contracts with different terms on normalized basis
- Analyze contract value independent of term length
- Evaluate subscription pricing effectiveness

### Growth Metrics
- Calculate ACV growth rates
- Track new ACV vs renewal ACV
- Measure ACV expansion and contraction

### Customer Value
- Analyze customer lifetime value using ACV
- Track ACV per customer and segment
- Evaluate customer acquisition cost vs ACV

---

## Related Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Source entity containing ACV data
- **[Contract](../entities/contract.md)** - Contract terms determining ACV calculation
- **[Customer](../entities/customer.md)** - Customer ACV contribution
- **[Product](../entities/product.md)** - Product ACV performance
- **[Sales Representative](../entities/sales-representative.md)** - Sales rep ACV credit

---

## Related Measures

- **[Total Contract Value USD](./total-contract-value-usd.md)** - Full contract value (ACV × Term)
- **[Booking Amount USD](./booking-amount-usd.md)** - Initial booking amount
- **[Quantity Sold](./quantity-sold.md)** - Volume component
- **[Discount Percentage](./discount-percentage.md)** - Pricing impact on ACV

---

## Calculation Relationships

```
ACV = TCV / Contract Term (Years)
TCV = ACV × Contract Term (Years)
Monthly Recurring Revenue (MRR) = ACV / 12
Quarterly Contract Value = ACV / 4
```

---

## Dimensional Analysis

Annual Contract Value USD can be analyzed across:

- **[Date](../entities/date.md)** - ACV trends over time
- **[Product](../entities/product.md)** - Product ACV performance
- **[Customer](../entities/customer.md)** - Customer segment ACV
- **[Geography](../entities/geography.md)** - Regional ACV distribution
- **[Partner](../entities/partner.md)** - Channel ACV contribution
- **[Sales Representative](../entities/sales-representative.md)** - Sales rep ACV performance
- **[Contract](../entities/contract.md)** - ACV by contract type and term

---

## Key Performance Indicators

- **Total ACV** - Sum of all annual contract values
- **Average ACV** - Mean ACV per transaction
- **ACV Growth Rate** - Period-over-period ACV change
- **New ACV** - ACV from new customer bookings
- **Renewal ACV** - ACV from contract renewals
- **ACV per Customer** - Average ACV per customer account

---

## Business Context

ACV is critical for subscription and SaaS business models as it:
- Provides normalized view of contract values
- Supports recurring revenue forecasting
- Enables comparison across different contract terms
- Drives valuation metrics for subscription businesses
- Supports customer lifetime value calculations

---

## Use Cases

### Subscription Business
- Track monthly recurring revenue (MRR = ACV / 12)
- Monitor annual recurring revenue (ARR = Total ACV)
- Analyze subscription growth and churn

### Sales Performance
- Measure sales rep performance on recurring revenue basis
- Track ACV quota attainment
- Compare new vs renewal ACV contribution

### Financial Planning
- Forecast future recurring revenue streams
- Model subscription revenue growth
- Support financial planning and budgeting

---

## Semantic Links

- [Measure Index](./index.md)
- [Metrics Overview](../metrics.md)
- [Booking Transaction Entity](../entities/booking-transaction.md)
- [Contract Entity](../entities/contract.md)
- [Main Index](../index.md)

---

## Metadata

**Measure ID**: MEA005  
**Entity ID**: ENT008  
**Technical Column**: acv_usd  
**Data Type**: Numeric  
**Aggregation**: SUM  
**Currency**: USD  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
