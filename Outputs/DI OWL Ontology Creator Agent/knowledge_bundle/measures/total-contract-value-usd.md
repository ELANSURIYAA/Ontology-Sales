---
title: Total Contract Value USD
type: measure
description: Total value of the full contract associated with the booking in U.S. dollars
resource: measures
tags: [measure, tcv, contract, revenue, total]
timestamp: 2026-07-28T00:00:00Z
---

# Total Contract Value USD

## Business Definition

Total Contract Value (TCV) USD represents the total value of the full contract associated with the booking in U.S. dollars. This measure captures the complete revenue commitment over the entire contract term and is essential for long-term revenue planning, deal size analysis, and contract value tracking.

---

## Technical Mapping

**Measure ID**: MEA006  
**Technical Column**: tcv_usd  
**Source Table**: QuoteToBooking.fact_bookings  
**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Data Type**: Numeric

---

## Aggregation

**Aggregation Type**: SUM  
**Description**: Total TCV is calculated by summing individual total contract values across selected dimensions

---

## Formula

```
Total Contract Value (TCV) = Booking Amount × Contract Term (Months) / 12
TCV = Annual Contract Value (ACV) × Contract Term (Years)
Total TCV = SUM(tcv_usd)
```

---

## Business Rules

1. TCV must be non-negative
2. TCV is expressed in U.S. dollars (USD)
3. TCV represents full contract value over entire term
4. TCV includes all committed revenue for contract duration
5. TCV is calculated at time of booking

---

## Analytical Usage

### Contract Value Analysis
- Track total contract values by customer and segment
- Analyze deal sizes and contract commitments
- Monitor large deal pipeline and closure

### Long-term Revenue Planning
- Forecast committed revenue over contract terms
- Model future revenue streams from existing contracts
- Support multi-year financial planning

### Deal Size Analysis
- Compare deal sizes across segments and products
- Identify large enterprise deals
- Track average contract values

### Sales Performance
- Measure sales representative performance on total deal value
- Track large deal closure rates
- Analyze deal size trends over time

---

## Related Entities

- **[Booking Transaction](../entities/booking-transaction.md)** - Source entity containing TCV data
- **[Contract](../entities/contract.md)** - Contract terms determining TCV
- **[Customer](../entities/customer.md)** - Customer contract values
- **[Product](../entities/product.md)** - Product contract performance
- **[Sales Representative](../entities/sales-representative.md)** - Sales rep TCV credit

---

## Related Measures

- **[Annual Contract Value USD](./annual-contract-value-usd.md)** - Annualized contract value (TCV / Term)
- **[Booking Amount USD](./booking-amount-usd.md)** - Initial booking amount
- **[Quantity Sold](./quantity-sold.md)** - Volume component
- **[Discount Percentage](./discount-percentage.md)** - Pricing impact on TCV

---

## Calculation Relationships

```
TCV = ACV × Contract Term (Years)
TCV = Booking Amount × Contract Term (Months) / 12
ACV = TCV / Contract Term (Years)
Average Contract Term = TCV / ACV
```

---

## Dimensional Analysis

Total Contract Value USD can be analyzed across:

- **[Date](../entities/date.md)** - TCV trends over time
- **[Product](../entities/product.md)** - Product TCV performance
- **[Customer](../entities/customer.md)** - Customer segment TCV
- **[Geography](../entities/geography.md)** - Regional TCV distribution
- **[Partner](../entities/partner.md)** - Channel TCV contribution
- **[Sales Representative](../entities/sales-representative.md)** - Sales rep TCV performance
- **[Contract](../entities/contract.md)** - TCV by contract type and term

---

## Key Performance Indicators

- **Total TCV** - Sum of all total contract values
- **Average TCV** - Mean TCV per transaction
- **TCV Growth Rate** - Period-over-period TCV change
- **Large Deal TCV** - TCV from deals above threshold
- **TCV per Customer** - Average TCV per customer account
- **TCV Pipeline** - Forecasted future TCV

---

## Business Context

TCV is important for enterprise sales as it:
- Captures full revenue commitment over contract life
- Supports long-term revenue forecasting
- Enables deal size and contract value analysis
- Drives compensation for large enterprise deals
- Provides visibility into committed future revenue

---

## Use Cases

### Enterprise Sales
- Track large enterprise deal values
- Monitor multi-year contract commitments
- Analyze strategic account contract values

### Revenue Planning
- Forecast committed revenue streams
- Model future revenue from existing contracts
- Support financial planning and budgeting

### Sales Compensation
- Calculate commissions based on total deal value
- Reward large deal closure
- Track TCV quota attainment

### Contract Management
- Monitor contract value portfolio
- Track contract renewals and expansions
- Analyze contract value retention

---

## Comparison with ACV

| Aspect | TCV | ACV |
|--------|-----|-----|
| Definition | Total contract value | Annualized contract value |
| Time Period | Full contract term | One year |
| Use Case | Deal size analysis | Recurring revenue tracking |
| Calculation | ACV × Term | TCV / Term |

---

## Semantic Links

- [Measure Index](./index.md)
- [Metrics Overview](../metrics.md)
- [Booking Transaction Entity](../entities/booking-transaction.md)
- [Contract Entity](../entities/contract.md)
- [Main Index](../index.md)

---

## Metadata

**Measure ID**: MEA006  
**Entity ID**: ENT008  
**Technical Column**: tcv_usd  
**Data Type**: Numeric  
**Aggregation**: SUM  
**Currency**: USD  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
