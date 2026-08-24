---
title: Renewal
type: glossary
description: Continuation or extension of an existing customer contract or subscription
resource: glossary
tags: [renewal, contract, retention, subscription]
timestamp: 2026-07-28T00:00:00Z
---

# Renewal

## Business Definition

Continuation or extension of an existing customer contract or subscription.

A renewal represents a customer's decision to continue their relationship and maintain their service or product entitlements beyond the original contract term.

---

## Business Meaning

Renewals are booking transactions where an existing customer extends or continues their contract or subscription for an additional term. Renewals are distinguished from net new business and represent customer retention and loyalty.

Renewals are critical for:
- Measuring customer retention and satisfaction
- Tracking recurring revenue streams
- Forecasting predictable revenue
- Evaluating customer success effectiveness
- Supporting subscription business models
- Calculating renewal rates and churn

Renewal bookings are identified by the is_renewal flag in the booking transaction data.

---

## Technical Mapping

**Source Entity**: [Bookings](../entities/bookings.md)

**Source Field**: is_renewal

**Related Entity**: [Contracts](../entities/contracts.md)

---

## Synonyms

- Contract renewal
- Subscription renewal
- Service renewal
- Contract extension
- Renewal booking

---

## Related Concepts

- [Net New Business](net-new-business.md)
- [Booking Transaction](booking-transaction.md)
- [Annual Contract Value](annual-contract-value.md)
- [Total Contract Value](total-contract-value.md)

---

## Related Entities

- [Bookings](../entities/bookings.md)
- [Contracts](../entities/contracts.md)
- [Customers](../entities/customers.md)

---

## Related Measures

- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)

---

## Usage Examples

- "Calculate renewal rate by customer segment"
- "Track renewal revenue trends over time"
- "Analyze renewal vs net new business mix"
- "Forecast upcoming renewal opportunities"

---

## Navigation

- [Return to Glossary Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
