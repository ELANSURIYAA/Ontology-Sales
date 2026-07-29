---
title: Partner Dimension
type: entity
description: Channel partner attributes used to analyze bookings by partner identity, type, and tier
resource: entities
tags: [okf, entity, partner, dimension, channel]
timestamp: 2026-07-28T00:00:00Z
---

# Partner Dimension

## Business Definition

The Partner Dimension stores channel partner attributes used to analyze bookings by partner identity, partner type, partner tier, and route to market. This dimension enables channel sales analytics and supports partner relationship management.

---

## Technical Mapping

**Source Schema**: quotetobooking  
**Source Table**: dim_partner  
**Entity Type**: Dimension  
**Grain**: One record per unique partner

---

## Attributes

- partner_key
- partner_id
- partner_name
- partner_type
- partner_tier
- route_to_market

---

## Primary Keys

- partner_key

---

## Foreign Keys

None (this is a dimension table)

---

## Relationships

### Outbound Relationships
- [Partner to Booking](../relationships/partner-to-booking.md) - One-to-Many relationship to Booking Fact

---

## Measures

All booking measures can be analyzed by partner attributes:

- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Related Concepts

### Related Entities
- [Booking Fact](booking-fact.md)

### Related Domains
- [Partner Management](../domains/partner-management.md)
- [Sales Transactions](../domains/sales-transactions.md)

### Related Glossary Terms
- [Partner Dimension](../glossary/partner-dimension.md)
- [Partner Key](../glossary/partner-key.md)
- [Partner ID](../glossary/partner-id.md)
- [Partner Name](../glossary/partner-name.md)
- [Partner Type](../glossary/partner-type.md)
- [Partner Tier](../glossary/partner-tier.md)
- [Route to Market](../glossary/route-to-market.md)

---

## Business Rules

1. Partner Key must be unique and not null
2. Partner ID must be unique and not null
3. Partner Name is required for all records
4. Partner Type must match approved partner type classifications
5. Partner Tier should reflect current certification level
6. Route to Market must align with partner type

---

## Attribute Details

### partner_key
- **Data Type**: integer
- **Nullable**: No
- **Primary Key**: Yes
- **Description**: Surrogate key that uniquely identifies a partner record in the partner dimension

### partner_id
- **Data Type**: character varying(20)
- **Nullable**: No
- **Description**: Business identifier assigned to the partner organization

### partner_name
- **Data Type**: character varying(60)
- **Nullable**: Yes
- **Description**: Name of the distributor, reseller, integrator, or direct channel partner involved in the booking

### partner_type
- **Data Type**: character varying(30)
- **Nullable**: Yes
- **Description**: Classification of the partner, such as distributor, value-added reseller, systems integrator, or direct

### partner_tier
- **Data Type**: character varying(30)
- **Nullable**: Yes
- **Description**: Tier or certification level assigned to the partner in the channel program

### route_to_market
- **Data Type**: character varying(20)
- **Nullable**: Yes
- **Description**: Sales route through which the booking was transacted, such as direct, reseller, or two-tier

---

## Analytical Use Cases

- Analyze sales performance by channel partner
- Track revenue by partner type and tier
- Evaluate route to market effectiveness
- Monitor partner program performance
- Identify top performing partners
- Support partner relationship management

---

## Data Quality Metrics

- **Completeness**: Partner Key and Partner ID must be 100% populated
- **Uniqueness**: Partner Key and Partner ID must be unique
- **Validity**: Partner Type and Route to Market must match approved values
- **Consistency**: Route to Market must align with Partner Type

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Bundle Index](../index.md)
