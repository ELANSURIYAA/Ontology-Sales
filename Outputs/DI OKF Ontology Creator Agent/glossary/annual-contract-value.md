---
title: Annual Contract Value
type: glossary
description: Annualized revenue value of a contract or subscription
resource: glossary
tags: [acv, contract, revenue, annualized]
timestamp: 2026-07-28T00:00:00Z
---

# Annual Contract Value

## Business Definition

Annualized revenue value of a contract or subscription.

ACV normalizes contract values to an annual basis, enabling consistent comparison of contracts with different durations and supporting recurring revenue analysis.

---

## Business Meaning

Annual Contract Value (ACV) represents the yearly revenue value of a customer contract or subscription. For multi-year contracts, ACV divides the total contract value by the number of years. For contracts shorter than one year, ACV may annualize the value to a 12-month equivalent.

ACV is a critical metric for:
- Comparing contracts with different terms
- Forecasting annual recurring revenue
- Tracking subscription business performance
- Evaluating customer lifetime value
- Supporting financial planning and budgeting

---

## Technical Mapping

**Source Entity**: [Bookings](../entities/bookings.md)

**Source Field**: acv_usd

**Related Entity**: [Contracts](../entities/contracts.md)

---

## Synonyms

- Annualized Contract Value
- Annual Recurring Revenue (ARR) component
- Yearly contract value
- Normalized contract value

---

## Related Concepts

- [Total Contract Value](total-contract-value.md)
- [Booking Transaction](booking-transaction.md)
- [Renewal](renewal.md)

---

## Related Entities

- [Bookings](../entities/bookings.md)
- [Contracts](../entities/contracts.md)

---

## Related Measures

- [Total ACV USD](../measures/total-acv-usd.md)

---

## Usage Examples

- "Calculate total ACV by customer segment"
- "Track ACV growth year-over-year"
- "Analyze average ACV per booking"
- "Forecast annual recurring revenue based on ACV"

---

## Navigation

- [Return to Glossary Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
