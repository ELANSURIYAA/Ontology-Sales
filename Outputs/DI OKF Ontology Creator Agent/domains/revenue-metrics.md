---
title: Revenue Metrics Domain
type: domain
description: Financial value attributes used to analyze booked revenue, annual contract value, and total contract value
resource: domains
tags: [okf, domain, revenue-metrics, revenue, acv, tcv]
timestamp: 2026-07-28T00:00:00Z
---

# Revenue Metrics Domain

## Business Definition

The Revenue Metrics domain encompasses financial value attributes used to analyze booked revenue, annual contract value, and total contract value. This domain provides the financial measurement context necessary for revenue analytics and financial reporting.

---

## Business Purpose

This domain enables business users to:

- Track total booked revenue
- Analyze recurring revenue (ACV)
- Measure total contract value (TCV)
- Support revenue forecasting
- Enable financial reporting and planning
- Measure deal size and contract value
- Analyze revenue composition and trends

---

## Domain Scope

### Included
- Booking amount (total transaction value)
- Annual contract value (annualized recurring revenue)
- Total contract value (full contract term value)
- Revenue measures and calculations

### Excluded
- Revenue recognition schedules
- Deferred revenue
- Recognized revenue versus booked revenue
- Revenue adjustments and credits
- Cost and profitability metrics

---

## Related Entities

### Primary Entities
- [Booking Fact](../entities/booking-fact.md)

---

## Related Measures

### Revenue Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

### Related Measures
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Relationships

All dimensional relationships to Booking Fact enable revenue analysis by dimension:
- [Customer to Booking](../relationships/customer-to-booking.md)
- [Product to Booking](../relationships/product-to-booking.md)
- [Partner to Booking](../relationships/partner-to-booking.md)
- [Geography to Booking](../relationships/geography-to-booking.md)
- [Sales Representative to Booking](../relationships/sales-representative-to-booking.md)
- [Contract to Booking](../relationships/contract-to-booking.md)
- [Date to Booking](../relationships/date-to-booking.md)

---

## Key Business Concepts

### Booking Amount
Total booked revenue amount in U.S. dollars for the transaction. This represents the total value of the booking at the time of transaction and is the primary revenue measure for sales performance.

### Annual Contract Value (ACV)
Annualized contract value in U.S. dollars used for recurring revenue analysis. ACV normalizes contract values to an annual basis, enabling consistent comparison of contracts with different terms.

**Calculation**: For multi-year contracts, ACV = Total Contract Value / Contract Term (years)

### Total Contract Value (TCV)
Total contract value in U.S. dollars over the full contract term. TCV represents the complete value of the contract over its entire duration.

**Relationship**: TCV ≥ ACV (TCV equals ACV for 1-year contracts)

### Revenue Hierarchy
```
Total Contract Value (TCV)
└── Annual Contract Value (ACV)
    └── Booking Amount
```

---

## Business Rules

1. Booking Amount must be greater than or equal to 0
2. Annual Contract Value must be greater than or equal to 0
3. Total Contract Value must be greater than or equal to Annual Contract Value
4. For 1-year contracts: TCV should equal ACV
5. For multi-year contracts: TCV should equal ACV × Contract Term (years)
6. Booking Amount should equal Quantity × Unit List Price × (1 - Discount %)

---

## Analytical Use Cases

### Revenue Performance Analysis
- Track total booking revenue by period
- Analyze revenue growth trends
- Compare actual revenue to targets and quotas
- Measure revenue contribution by dimension

### Recurring Revenue Analysis
- Monitor Annual Contract Value (ACV) trends
- Analyze recurring versus one-time revenue
- Track subscription revenue growth
- Support recurring revenue forecasting

### Contract Value Analysis
- Analyze Total Contract Value (TCV) by segment
- Track average deal size trends
- Compare contract values across dimensions
- Identify large deal opportunities

### Revenue Composition Analysis
- Analyze revenue mix by product, customer, and partner
- Track revenue concentration and diversification
- Identify revenue drivers and contributors
- Support portfolio optimization

### Financial Forecasting
- Forecast future revenue based on bookings
- Project ACV and TCV trends
- Support annual and quarterly planning
- Enable pipeline to revenue conversion analysis

---

## Data Quality Metrics

### Completeness
- Booking Amount should be populated (>99% target)
- Annual Contract Value should be populated (>95% target)
- Total Contract Value should be populated (>95% target)

### Accuracy
- Booking Amount must be non-negative
- ACV must be non-negative
- TCV must be greater than or equal to ACV
- Revenue calculations must reconcile with source systems
- Revenue measures must align with contract terms

### Consistency
- TCV should equal or exceed ACV
- For 1-year contracts, TCV should equal ACV
- Booking Amount should reconcile with quantity and pricing
- Revenue measures must be consistent across all bookings

---

## Technical Implementation

### Source System
- **Schema**: quotetobooking
- **Table**: fact_bookings
- **Revenue Attributes**: booking_amount_usd, acv_usd, tcv_usd

### Key Attributes
- Booking Amount USD (numeric(14,2))
- Annual Contract Value USD (numeric(14,2))
- Total Contract Value USD (numeric(14,2))

### Calculated Metrics
- Average Deal Size = Sum(Booking Amount) / Count(Bookings)
- ACV to TCV Ratio = Sum(ACV) / Sum(TCV)
- Revenue per Customer = Sum(Booking Amount) / Count(Distinct Customers)

---

## Semantic Links

### Related Domains
- [Sales Transactions](sales-transactions.md)
- [Contract Management](contract-management.md)
- [Pricing](pricing.md)
- [Customer Management](customer-management.md)
- [Product Management](product-management.md)

### Related Glossary Terms
- [Booking Amount USD](../glossary/booking-amount-usd.md)
- [Annual Contract Value USD](../glossary/annual-contract-value-usd.md)
- [Total Contract Value USD](../glossary/total-contract-value-usd.md)
- [Booking Fact](../glossary/booking-fact.md)

---

## Navigation

- [Back to Domains Index](index.md)
- [Back to Bundle Index](../index.md)
