---
title: Partner Type
type: glossary
description: Classification of partner such as distributor, reseller, or systems integrator
resource: glossary
tags: [partner-type, partner, channel]
timestamp: 2026-07-28T00:00:00Z
---

# Partner Type

## Business Definition

Partner Type is the classification of sales partners based on their role in the sales and distribution channel. Common partner types include distributor, reseller, systems integrator, and direct channel.

---

## Business Meaning

Partner Type is used to:
- Categorize partners by their role in the sales process
- Support channel strategy and partner program design
- Enable partner performance analysis by type
- Guide partner recruitment and development
- Optimize channel mix and go-to-market strategies
- Support partner-specific pricing and incentives

Common partner types include:
- **Distributor**: Wholesale partners who sell to resellers
- **Reseller**: Partners who sell directly to end customers
- **Systems Integrator**: Partners who provide implementation and integration services
- **Direct Channel**: Direct sales without partner involvement
- **Value-Added Reseller (VAR)**: Resellers who add services or customization
- **Managed Service Provider (MSP)**: Partners who provide managed services

---

## Technical Mapping

**Source Entity**: [Partners](../entities/partners.md)

**Source Field**: partner_type

---

## Synonyms

- Channel Type
- Partner Category
- Partner Classification
- Channel Partner Type
- Distribution Type

---

## Related Concepts

- [Route to Market](./route-to-market.md) - Sales channel path
- [Booking Transaction](./booking-transaction.md) - Transactions analyzed by partner type

---

## Related Entities

- [Partners](../entities/partners.md) - Contains partner type classification

---

## Related Measures

All booking measures can be analyzed by partner type:
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Average Discount Percentage](../measures/average-discount-pct.md)

---

## Usage Context

Partner Type is used for:
- Channel strategy development
- Partner program design
- Partner performance analysis
- Channel mix optimization
- Partner recruitment targeting
- Pricing and margin management
- Channel conflict resolution

---

## Business Rules

1. Each partner is assigned to a partner type
2. Partner type reflects the partner's primary role in the channel
3. Partner type classification is standardized across the organization
4. Partners may evolve to different types over time

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
