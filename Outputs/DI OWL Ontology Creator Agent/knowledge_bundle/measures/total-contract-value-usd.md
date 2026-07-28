---
title: Total Contract Value USD
type: measure
description: Total value of the full contract associated with the booking in U.S. dollars
resource: measures
tags: [measure, revenue, tcv, contract-value, total-value, usd]
timestamp: 2026-07-28T00:00:00Z
---

# Total Contract Value USD

## Business Definition

Total value of the full contract associated with the booking in U.S. dollars. This measure represents the complete revenue commitment over the entire contract term and supports analysis of long-term revenue potential, contract commitments, and customer lifetime value.

---

## Measure Details

**Measure ID**: MEA006  
**Measure Type**: Revenue Metric  
**Aggregation Type**: SUM  
**Unit of Measure**: USD (U.S. Dollars)

---

## Technical Mapping

**Source Entity**: [Booking Transaction](../entities/booking-transaction.md)  
**Source Table**: QuoteToBooking.fact_bookings  
**Source Column**: tcv_usd  
**Data Type**: numeric

---

## Formula

```
Total Contract Value USD = SUM(tcv_usd)
```

Alternatively calculated as:
```
Total Contract Value USD = Annual Contract Value USD × Contract Term Months / 12
```

---

## Related Entities

### Source Entity
- [Booking Transaction](../entities/booking-transaction.md) - Fact table containing TCV values

### Analysis Dimensions
- [Contract](../entities/contract.md) - Analyze TCV by contract type, term, and coverage level
- [Customer](../entities/customer.md) - Evaluate TCV by customer segment and account tier
- [Product](../entities/product.md) - Assess TCV by product family and offer type
- [Date](../entities/date.md) - Track TCV trends over time
- [Geography](../entities/geography.md) - Compare TCV across regions
- [Partner](../entities/partner.md) - Evaluate partner TCV contribution
- [Sales Representative](../entities/sales-representative.md) - Measure sales team TCV performance

---

## Related Domains

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Aggregation**: Always use SUM aggregation for TCV
2. **Currency**: All values are in U.S. dollars (USD)
3. **Full Term Value**: Represents total revenue over complete contract duration
4. **Long-Term Commitment**: Captures customer commitment over contract lifetime
5. **Non-Negative**: TCV values should be positive
6. **Contract Relationship**: Related to ACV through contract term duration

---

## Usage Examples

### Total TCV by Customer Segment
Calculate total contract value by customer segment to assess long-term revenue commitments.

### TCV by Contract Type
Analyze TCV by contract type to understand which agreement structures drive largest commitments.

### TCV Growth Tracking
Track TCV trends over fiscal periods to measure growth in contracted revenue.

### Average Contract Size
Calculate average TCV to understand typical contract commitment sizes.

### Customer Lifetime Value Analysis
Use TCV as a component of customer lifetime value calculations.

---

## Related Measures

### Complementary Measures
- [Annual Contract Value USD](annual-contract-value-usd.md) - Annualized contract value
- [Booking Amount USD](booking-amount-usd.md) - Total booking revenue
- [Quantity Sold](quantity-sold.md) - Volume of products sold

### Calculated Metrics
- **Average TCV per Customer** = SUM(TCV USD) / COUNT(DISTINCT Customer Key)
- **Average Contract Term** = SUM(TCV USD) / SUM(ACV USD)
- **TCV Growth Rate** = (Current Period TCV - Prior Period TCV) / Prior Period TCV
- **TCV per Sales Rep** = SUM(TCV USD) / COUNT(DISTINCT Sales Rep Key)

---

## Related Glossary Terms

- [Total Contract Value USD](../glossary/total-contract-value-usd.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Contract](../glossary/contract.md)

---

## Analysis Guidelines

### Best Practices
- Use SUM aggregation across all dimensions
- Analyze alongside ACV to understand contract duration
- Track TCV for long-term revenue forecasting
- Compare across customer segments to identify high-value customers
- Use for pipeline and opportunity analysis

### Common Analysis Patterns
- Total TCV by fiscal quarter and year
- TCV by customer segment and account tier
- Contract type TCV comparison
- Average TCV by product family
- Geographic TCV distribution
- New vs renewal TCV analysis

### Key Performance Indicators
- **Total TCV**: SUM(Total Contract Value USD)
- **TCV Growth**: (Current Period TCV - Prior Period TCV) / Prior Period TCV
- **Average TCV**: SUM(TCV) / COUNT(Contracts)
- **Average Contract Term**: TCV / ACV

---

## Relationship to Other Metrics

### TCV vs ACV
- TCV represents total contract value over full term
- ACV represents annualized value
- Relationship: TCV = ACV × (Contract Term Months / 12)

### TCV vs Booking Amount
- TCV represents long-term contract commitment
- Booking Amount represents immediate revenue recognition
- Both metrics provide different perspectives on revenue

---

## Navigation

- [View Measures Index](index.md)
- [View Booking Transaction Entity](../entities/booking-transaction.md)
- [View Contract Entity](../entities/contract.md)
- [View Related Measures](index.md#revenue-measures)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Measure ID**: MEA006  
**Category**: Revenue Metric  
**Source Entity**: Booking Transaction  
**Aggregation**: SUM  
**Last Updated**: 2026-07-28T00:00:00Z
