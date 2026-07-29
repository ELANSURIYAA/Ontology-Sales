---
title: Partner
type: entity
description: Channel and direct partners involved in the sales process including partner type, partner tier, and route to market
resource: entities
tags: [partner, channel, reseller, distributor, dimension]
timestamp: 2026-07-28T00:00:00Z
---

# Partner

## Business Definition

Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market. Partners are organizations that facilitate sales transactions and provide customer access to products and services.

---

## Entity Identifier

**Entity ID:** ENT005  
**Domain:** [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_partner  
**Table Type:** Dimension Table

---

## Attributes

- **Partner Key** - Surrogate key that uniquely identifies a partner record in the partner dimension
- **Partner ID** - Business identifier assigned to the partner organization
- **Partner Name** - Name of the partner organization involved in the transaction
- **Partner Type** - Classifies the partner by operating model, such as distributor, reseller, systems integrator, or direct
- **Partner Tier** - Indicates the certification, authorization, or strategic tier assigned to the partner
- **Route to Market** - Describes the sales delivery path through which the product or service reached the customer

---

## Primary Keys

- **Partner Key** (partner_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- **[Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)** - One-to-Many relationship linking partners to booking transactions

---

## Measures

Partners are analyzed using measures from related [Booking Transaction](./booking-transaction.md) entity:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)

---

## Business Rules

1. Each partner must have a unique Partner Key
2. Partner ID serves as the business identifier for the partner organization
3. Partner Type categorizes the partner's operating model
4. Partner Tier indicates certification level and strategic importance
5. Route to Market defines the sales channel path
6. Partners facilitate transactions between vendors and customers

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Transactions facilitated by partners
- [Customer](./customer.md) - Customers served by partners
- [Product](./product.md) - Products sold through partners
- [Geography](./geography.md) - Geographic markets where partners operate
- [Sales Representative](./sales-representative.md) - Sales representatives working with partners

---

## Glossary Terms

- [Partner](../glossary/partner.md)
- [Partner Key](../glossary/partner-key.md)
- [Partner ID](../glossary/partner-id.md)
- [Partner Name](../glossary/partner-name.md)
- [Partner Type](../glossary/partner-type.md)
- [Partner Tier](../glossary/partner-tier.md)
- [Route to Market](../glossary/route-to-market.md)

---

## Navigation

- [Return to Entities Index](./index.md)
- [Return to Bundle Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
- [View Relationships](../relationships/index.md)
