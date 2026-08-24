---
title: Annual Contract Value
type: glossary
description: The annualized revenue value of a contract for subscription and recurring revenue analysis
resource: glossary
tags: [acv, contract-value, revenue, subscription]
timestamp: 2026-07-28T00:00:00Z
---

# Annual Contract Value

## Business Definition

Annual Contract Value (ACV) is the annualized revenue value of a contract, representing the yearly recurring revenue expected from a customer contract. ACV normalizes contract values to an annual basis, enabling consistent comparison and analysis of contracts with different term lengths.

---

## Business Meaning

ACV is a critical metric for subscription and recurring revenue businesses. It provides a standardized measure of contract value by expressing multi-year contracts on an annual basis, making it easier to:
- Compare contracts with different term lengths
- Track recurring revenue trends
- Forecast future revenue
- Value the business based on recurring revenue streams
- Measure customer lifetime value
- Support investor and board reporting

For a contract with a total value of $120,000 over 3 years, the ACV would be $40,000 per year.

---

## Technical Mapping

**Source Entity**: [Bookings](../entities/bookings.md)

**Source Field**: acv_usd

**Calculation**: Total Contract Value / Contract Term in Years

---

## Synonyms

- ARR (Annual Recurring Revenue)
- Annualized Contract Value
- Annual Revenue
- Yearly Contract Value

---

## Related Concepts

- [Total Contract Value](./total-contract-value.md) - Full contract value over entire term
- [Booking Amount](./booking-amount.md) - Total booked revenue
- [Booking Transaction](./booking-transaction.md) - Transaction containing ACV
- [Renewal](./renewal.md) - Renewal contracts contribute to recurring ACV

---

## Related Entities

- [Bookings](../entities/bookings.md) - Contains ACV values
- [Contracts](../entities/contracts.md) - Contract terms used to calculate ACV

---

## Related Measures

- [Total ACV USD](../measures/total-acv-usd.md) - Sum of all ACV values
- [Total TCV USD](../measures/total-tcv-usd.md) - Sum of all TCV values
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md) - Total booking revenue

---

## Usage Context

ACV is used for:
- Subscription business performance tracking
- Recurring revenue analysis
- SaaS metrics and KPIs
- Business valuation
- Investor reporting
- Revenue forecasting
- Customer lifetime value calculation
- Churn and retention analysis

---

## Business Rules

1. ACV represents the annual portion of a contract's total value
2. For annual contracts, ACV equals the booking amount
3. For multi-year contracts, ACV = TCV / (term_months / 12)
4. ACV is expressed in US dollars
5. ACV must be non-negative
6. ACV is most relevant for subscription and recurring revenue contracts

---

## Calculation Example

**Example 1: Annual Contract**
- Contract Term: 12 months
- Total Contract Value: $50,000
- ACV: $50,000

**Example 2: Multi-Year Contract**
- Contract Term: 36 months (3 years)
- Total Contract Value: $150,000
- ACV: $150,000 / 3 = $50,000

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
