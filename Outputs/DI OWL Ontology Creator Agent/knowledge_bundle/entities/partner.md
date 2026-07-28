---
title: Partner
type: entity
description: Channel and direct partners involved in the sales process including partner type, partner tier, and route to market
resource: entities
tags: [entity, dimension, partner, channel, reseller, distributor]
timestamp: 2026-07-28T00:00:00Z
---

# Partner

## Business Definition

Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_partner

**Source System**: QuoteToBooking

**Entity Type**: Dimension

---

## Attributes

- **Partner Key** (partner_key): Surrogate key that uniquely identifies a partner record in the partner dimension
- **Partner ID** (partner_id): Business identifier assigned to the partner organization
- **Partner Name** (partner_name): Name of the partner organization involved in the transaction
- **Partner Type** (partner_type): Classifies the partner by operating model, such as distributor, reseller, systems integrator, or direct
- **Partner Tier** (partner_tier): Indicates the certification, authorization, or strategic tier assigned to the partner
- **Route to Market** (route_to_market): Describes the sales delivery path through which the product or service reached the customer

---

## Primary Keys

- **Partner Key** (partner_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- **[Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)**: One-to-Many relationship linking partners to booking transactions

### Related Entities

- [Booking Transaction](booking-transaction.md): Fact entity that references this dimension
- [Customer](customer.md): Related through sales transactions
- [Product](product.md): Related through product sales

---

## Measures

This dimension supports analysis of the following measures:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Concepts

- [Partner](../glossary/partner.md)
- [Partner Key](../glossary/partner-key.md)
- [Partner ID](../glossary/partner-id.md)
- [Partner Name](../glossary/partner-name.md)
- [Partner Type](../glossary/partner-type.md)
- [Partner Tier](../glossary/partner-tier.md)
- [Route to Market](../glossary/route-to-market.md)

---

## Business Rules

1. Partner Key is a surrogate key and must be unique
2. Partner ID is the business identifier for the partner organization
3. Partner Name is the official organization name
4. Partner Type classifies partners by operating model (distributor, reseller, systems integrator, direct)
5. Partner Tier indicates certification, authorization, or strategic level
6. Route to Market describes the sales delivery path
7. Every booking transaction must reference a valid partner
8. Partner attributes support channel performance analysis

---

## Usage Examples

**Analysis by Partner Type**:
- Compare booking revenue across distributors, resellers, and systems integrators
- Analyze direct vs. indirect sales performance
- Measure channel mix and contribution

**Analysis by Partner Tier**:
- Evaluate performance by partner certification level
- Compare strategic vs. standard partner revenue
- Analyze partner tier effectiveness

**Analysis by Route to Market**:
- Measure booking amounts by sales delivery path
- Compare direct vs. channel routes
- Analyze route effectiveness by product or geography

**Partner Performance**:
- Identify top-performing partners by booking revenue
- Analyze partner product mix
- Compare discount rates by partner type

**Channel Strategy**:
- Evaluate channel coverage by geography
- Analyze partner distribution by customer segment
- Measure partner engagement and productivity

---

## Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Main Index](../index.md)
- [View Relationships](../relationships/index.md)
- [View Measures](../measures/index.md)
- [View Glossary](../glossary/index.md)
