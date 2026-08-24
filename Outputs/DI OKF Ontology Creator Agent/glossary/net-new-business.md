---
title: Net New Business
type: glossary
description: Revenue from new customer acquisitions or expansion sales to existing customers
resource: glossary
tags: [net-new, acquisition, expansion, growth]
timestamp: 2026-07-28T00:00:00Z
---

# Net New Business

## Business Definition

Revenue from new customer acquisitions or expansion sales to existing customers.

Net new business represents growth revenue that is not from contract renewals, including first-time customer purchases and upsell/cross-sell to existing customers.

---

## Business Meaning

Net new business captures booking transactions that represent new revenue streams rather than renewals of existing contracts. This includes:
- New customer acquisitions (first purchase)
- Expansion sales to existing customers (additional products or services)
- Upsell transactions (higher-tier offerings)
- Cross-sell transactions (complementary products)

Net new business is critical for:
- Measuring sales growth and market expansion
- Tracking new customer acquisition effectiveness
- Evaluating expansion and upsell success
- Supporting growth forecasting
- Calculating customer acquisition costs
- Assessing market penetration

Net new bookings are identified by is_renewal = 0 in the booking transaction data.

---

## Technical Mapping

**Source Entity**: [Bookings](../entities/bookings.md)

**Source Field**: is_renewal (value = 0)

---

## Synonyms

- New business
- New bookings
- Non-renewal business
- Growth bookings
- Acquisition revenue

---

## Related Concepts

- [Renewal](renewal.md)
- [Booking Transaction](booking-transaction.md)
- [Annual Contract Value](annual-contract-value.md)

---

## Related Entities

- [Bookings](../entities/bookings.md)
- [Customers](../entities/customers.md)

---

## Related Measures

- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

---

## Usage Examples

- "Calculate net new business by customer segment"
- "Track net new vs renewal revenue mix"
- "Analyze net new business growth trends"
- "Forecast new customer acquisition revenue"

---

## Navigation

- [Return to Glossary Index](index.md)
- [Return to Main Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
