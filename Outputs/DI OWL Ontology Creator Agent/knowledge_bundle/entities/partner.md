---
title: Partner
type: entity
description: Business entity representing channel and direct partners involved in the sales process
resource: entities
tags: [entity, dimension, partner, channel, reseller, distributor]
timestamp: 2026-07-28T00:00:00Z
---

# Partner

## Business Definition

Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market. The Partner entity enables analysis of partner ecosystem performance, channel effectiveness, and route-to-market strategies.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_partner  
**Entity Type**: Dimension  
**Entity ID**: ENT005

---

## Attributes

- **Partner Key** (partner_key) - integer, NOT NULL
- **Partner ID** (partner_id) - character varying(20), NOT NULL
- **Partner Name** (partner_name) - character varying(60), NULL
- **Partner Type** (partner_type) - character varying(30), NULL
- **Partner Tier** (partner_tier) - character varying(30), NULL
- **Route to Market** (route_to_market) - character varying(20), NULL

---

## Primary Keys

- **Partner Key** (partner_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- [Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md) - Links partners to booking transactions (One-to-Many)

---

## Measures

Partners are analyzed using measures from related booking transactions:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Concepts

### Related Entities
- [Booking Transaction](booking-transaction.md) - Booking transactions involving this partner
- [Customer](customer.md) - Customers served through partners
- [Product](product.md) - Products sold through partners

### Related Glossary Terms
- [Partner](../glossary/partner.md)
- [Partner Key](../glossary/partner-key.md)
- [Partner ID](../glossary/partner-id.md)
- [Partner Name](../glossary/partner-name.md)
- [Partner Type](../glossary/partner-type.md)
- [Partner Tier](../glossary/partner-tier.md)
- [Route to Market](../glossary/route-to-market.md)

### Related Domains
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Uniqueness**: Each partner record is uniquely identified by Partner Key
2. **Business Identifier**: Partner ID serves as the business identifier for the partner organization
3. **Partner Classification**: Partner Type classifies partners by operating model (distributor, reseller, systems integrator, direct)
4. **Partner Tiering**: Partner Tier indicates certification, authorization, or strategic level assigned to the partner
5. **Route to Market**: Describes the sales delivery path through which products reach customers
6. **Partner Ecosystem**: Partners play a critical role in extending market reach and customer coverage

---

## Usage Examples

### Partner Performance Analysis
Analyze booking amounts by partner to identify top-performing partners and assess partner contribution to revenue.

### Partner Type Analysis
Compare booking performance across partner types (distributor, reseller, systems integrator, direct) to evaluate channel effectiveness.

### Partner Tier Analysis
Evaluate booking amounts and average deal sizes by partner tier to assess the impact of partner certification and investment.

### Route to Market Analysis
Analyze booking performance by route to market to optimize channel strategy and resource allocation.

### Partner Discount Analysis
Monitor average discount percentages by partner type and tier to ensure pricing discipline and margin protection.

---

## Data Quality Notes

- Partner Key is mandatory and serves as the primary key
- Partner ID is mandatory and serves as the business identifier
- Partner Name should be populated for all active partner records
- Partner Type, Tier, and Route to Market classifications support channel analysis
- NULL values in descriptive attributes may indicate incomplete partner profiles
- Partner dimension should include both channel partners and direct sales representation

---

## Navigation

- [View Entity Index](index.md)
- [View Related Relationships](../relationships/index.md)
- [View Related Measures](../measures/index.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Entity ID**: ENT005  
**Domain**: Sales Bookings and Revenue Analytics  
**Entity Type**: Dimension  
**Attribute Count**: 6  
**Relationship Count**: 1  
**Last Updated**: 2026-07-28T00:00:00Z
