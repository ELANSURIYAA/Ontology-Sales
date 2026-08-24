---
title: Renewal
type: glossary
description: A booking transaction representing the continuation of an existing customer contract
resource: glossary
tags: [renewal, retention, recurring-revenue]
timestamp: 2026-07-28T00:00:00Z
---

# Renewal

## Business Definition

A Renewal is a booking transaction that represents the continuation of an existing customer contract or subscription. Renewals indicate that a customer has chosen to extend their relationship and continue using products or services beyond the initial contract term.

---

## Business Meaning

Renewals are critical indicators of:
- Customer satisfaction and retention
- Recurring revenue stability
- Customer lifetime value
- Product-market fit
- Customer success effectiveness

Renewal transactions differ from net new business in that they represent revenue from existing customers who are continuing their relationship, rather than new customer acquisition or expansion into new products.

Renewals are essential for:
- Tracking customer retention rates
- Forecasting recurring revenue
- Measuring customer success
- Calculating churn rates
- Evaluating product stickiness
- Supporting subscription business models

---

## Technical Mapping

**Source Entity**: [Bookings](../entities/bookings.md)

**Source Field**: is_renewal (flag = 1)

**Identification**: Booking transactions where is_renewal = 1

---

## Synonyms

- Contract Renewal
- Subscription Renewal
- Renewal Transaction
- Renewal Booking
- Repeat Business

---

## Related Concepts

- [Net New Business](./net-new-business.md) - Complementary concept for new customer revenue
- [Booking Transaction](./booking-transaction.md) - Parent concept
- [Annual Contract Value](./annual-contract-value.md) - Renewal ACV tracking
- [Booking Amount](./booking-amount.md) - Renewal revenue value

---

## Related Entities

- [Bookings](../entities/bookings.md) - Contains renewal flag
- [Contracts](../entities/contracts.md) - Contract terms including auto-renewal settings
- [Customers](../entities/customers.md) - Customers with renewal transactions

---

## Related Measures

- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md) - Total renewal revenue
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md) - Complementary net new revenue
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md) - Total revenue (renewal + net new)

---

## Usage Context

Renewals are used for:
- Customer retention analysis
- Churn rate calculation
- Recurring revenue forecasting
- Customer success metrics
- Renewal rate tracking
- Customer lifetime value calculation
- Subscription business health assessment
- Revenue mix analysis (renewal vs. net new)

---

## Business Rules

1. A booking is classified as a renewal when is_renewal = 1
2. Renewals represent continuation of existing customer relationships
3. Each booking is either a renewal or net new, not both
4. Renewal classification is mutually exclusive with net new classification
5. Renewals contribute to recurring revenue metrics

---

## Key Metrics

### Renewal Rate (by Revenue)
```
Renewal Booking Amount / (Renewal Booking Amount + Churned Revenue)
```

### Renewal Revenue Mix
```
Renewal Booking Amount / Total Booking Amount
```

### Renewal Growth
```
(Current Period Renewal Amount - Prior Period Renewal Amount) / Prior Period Renewal Amount
```

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
