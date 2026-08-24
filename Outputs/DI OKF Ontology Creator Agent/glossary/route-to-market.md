---
title: Route to Market
type: glossary
description: Sales channel path through which products or services are sold to customers
resource: glossary
tags: [route-to-market, channel, distribution]
timestamp: 2026-07-28T00:00:00Z
---

# Route to Market

## Business Definition

Route to Market is the sales channel path through which products or services are sold to customers. It represents the distribution strategy and channel model used to reach end customers.

---

## Business Meaning

Route to Market is used to:
- Define how products reach customers
- Support channel strategy and optimization
- Enable route-specific performance analysis
- Guide channel investment decisions
- Optimize distribution efficiency
- Support pricing and margin strategies by channel

Common routes to market include:
- **Direct Sales**: Company sales force selling directly to customers
- **Two-Tier Distribution**: Manufacturer → Distributor → Reseller → Customer
- **One-Tier Distribution**: Manufacturer → Reseller → Customer
- **Online/E-commerce**: Direct online sales channel
- **Partner-Led**: Partners drive the entire sales process
- **Hybrid**: Combination of direct and indirect channels

---

## Technical Mapping

**Source Entity**: [Partners](../entities/partners.md)

**Source Field**: route_to_market

---

## Synonyms

- Channel Path
- Distribution Channel
- Sales Channel
- Go-to-Market Route
- Channel Model

---

## Related Concepts

- [Partner Type](./partner-type.md) - Classification of partners in the route
- [Booking Transaction](./booking-transaction.md) - Transactions analyzed by route to market

---

## Related Entities

- [Partners](../entities/partners.md) - Contains route to market classification

---

## Related Measures

All booking measures can be analyzed by route to market:
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Average Discount Percentage](../measures/average-discount-pct.md)

---

## Usage Context

Route to Market is used for:
- Channel strategy development
- Distribution efficiency analysis
- Channel mix optimization
- Margin and pricing management
- Channel conflict management
- Market coverage planning
- Channel investment allocation

---

## Business Rules

1. Each booking transaction is associated with a route to market
2. Route to market reflects the actual channel path used
3. Route classification is standardized across the organization
4. Multiple routes may be used for different products or segments

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
