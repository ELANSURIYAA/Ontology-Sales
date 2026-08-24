---
title: Total Contract Value
type: glossary
description: The full contract value over the entire contract term for long-term revenue planning
resource: glossary
tags: [tcv, contract-value, revenue]
timestamp: 2026-07-28T00:00:00Z
---

# Total Contract Value

## Business Definition

Total Contract Value (TCV) is the full revenue value of a contract over its entire term. TCV represents the total amount a customer commits to pay over the complete duration of the contract, providing a comprehensive view of long-term revenue commitments.

---

## Business Meaning

TCV is essential for understanding the full financial impact of customer contracts, especially for multi-year agreements. It captures:
- The complete revenue commitment from a customer
- Long-term revenue potential
- Total deal size regardless of contract length
- Full value of multi-year agreements

TCV is particularly important for:
- Long-term revenue planning and forecasting
- Pipeline and opportunity valuation
- Deal size analysis
- Customer lifetime value assessment
- Strategic account management

For a 3-year contract worth $40,000 per year, the TCV would be $120,000.

---

## Technical Mapping

**Source Entity**: [Bookings](../entities/bookings.md)

**Source Field**: tcv_usd

**Calculation**: Annual Contract Value × Contract Term in Years

---

## Synonyms

- Total Contract Revenue
- Contract Lifetime Value
- Full Contract Value
- Total Deal Value

---

## Related Concepts

- [Annual Contract Value](./annual-contract-value.md) - Annualized portion of TCV
- [Booking Amount](./booking-amount.md) - Total booked revenue
- [Booking Transaction](./booking-transaction.md) - Transaction containing TCV

---

## Related Entities

- [Bookings](../entities/bookings.md) - Contains TCV values
- [Contracts](../entities/contracts.md) - Contract terms used to calculate TCV

---

## Related Measures

- [Total TCV USD](../measures/total-tcv-usd.md) - Sum of all TCV values
- [Total ACV USD](../measures/total-acv-usd.md) - Sum of all ACV values
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md) - Total booking revenue

---

## Usage Context

TCV is used for:
- Long-term revenue forecasting
- Multi-year contract analysis
- Deal size evaluation
- Pipeline valuation
- Customer lifetime value calculation
- Strategic account planning
- Contract portfolio management
- Revenue commitment tracking

---

## Business Rules

1. TCV represents the total value over the complete contract term
2. For annual contracts, TCV equals the booking amount
3. For multi-year contracts, TCV = ACV × (term_months / 12)
4. TCV is expressed in US dollars
5. TCV must be non-negative
6. TCV is most relevant for multi-year contracts

---

## Calculation Example

**Example 1: Annual Contract**
- Contract Term: 12 months
- Annual Contract Value: $50,000
- TCV: $50,000

**Example 2: Multi-Year Contract**
- Contract Term: 36 months (3 years)
- Annual Contract Value: $50,000
- TCV: $50,000 × 3 = $150,000

---

## Relationship to ACV

TCV and ACV are complementary metrics:
- **ACV** provides a normalized annual view for comparison
- **TCV** provides the total commitment for planning
- **Relationship**: TCV = ACV × Contract Term (in years)
- **Average Contract Term**: TCV / ACV

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
