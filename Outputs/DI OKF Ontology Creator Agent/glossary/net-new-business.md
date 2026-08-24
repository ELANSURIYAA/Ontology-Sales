---
title: Net New Business
type: glossary
description: A booking transaction representing new customer acquisition or expansion
resource: glossary
tags: [net-new, growth, acquisition]
timestamp: 2026-07-28T00:00:00Z
---

# Net New Business

## Business Definition

Net New Business refers to booking transactions that represent new customer acquisition or expansion into new products and services with existing customers. Net new bookings indicate business growth through new customer relationships or increased spending from current customers.

---

## Business Meaning

Net New Business is a critical indicator of:
- Business growth and expansion
- Sales effectiveness in acquiring new customers
- Market penetration and share growth
- Product adoption and expansion
- Sales team performance on new business

Net new transactions differ from renewals in that they represent incremental revenue from:
- Brand new customers (new logos)
- Existing customers purchasing additional products
- Existing customers expanding usage or licenses
- Cross-sell and upsell opportunities

Net new business is essential for:
- Tracking customer acquisition
- Measuring market expansion
- Evaluating new product adoption
- Assessing sales pipeline effectiveness
- Supporting growth strategies
- Balancing revenue mix with renewals

---

## Technical Mapping

**Source Entity**: [Bookings](../entities/bookings.md)

**Source Field**: is_renewal (flag = 0)

**Identification**: Booking transactions where is_renewal = 0

---

## Synonyms

- New Business
- New Customer Revenue
- Net New Revenue
- New Logo Revenue
- Expansion Revenue

---

## Related Concepts

- [Renewal](./renewal.md) - Complementary concept for existing customer retention
- [Booking Transaction](./booking-transaction.md) - Parent concept
- [Annual Contract Value](./annual-contract-value.md) - Net new ACV tracking
- [Booking Amount](./booking-amount.md) - Net new revenue value

---

## Related Entities

- [Bookings](../entities/bookings.md) - Contains renewal flag (0 for net new)
- [Customers](../entities/customers.md) - New and existing customers
- [Products](../entities/products.md) - Products sold as net new business

---

## Related Measures

- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md) - Total net new revenue
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md) - Complementary renewal revenue
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md) - Total revenue (renewal + net new)

---

## Usage Context

Net New Business is used for:
- Growth analysis and tracking
- Customer acquisition metrics
- Sales pipeline conversion analysis
- Market expansion assessment
- Product adoption tracking
- Revenue mix analysis (net new vs. renewal)
- Sales compensation and incentives
- Strategic planning and forecasting

---

## Business Rules

1. A booking is classified as net new when is_renewal = 0
2. Net new represents new customer acquisition or expansion
3. Each booking is either net new or renewal, not both
4. Net new classification is mutually exclusive with renewal classification
5. Net new contributes to growth metrics

---

## Key Metrics

### Net New Rate (by Revenue)
```
Net New Booking Amount / Total Booking Amount
```

### Net New Growth
```
(Current Period Net New Amount - Prior Period Net New Amount) / Prior Period Net New Amount
```

### Revenue Mix
```
Total Booking Amount = Renewal Booking Amount + Net New Booking Amount
```

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
