---
title: Partners
type: entity
description: Stores information about direct and indirect sales partners involved in fulfilling customer bookings, including partner identity, type, tier, and route to market
resource: entities
tags: [partners, dimension, partner-type, route-to-market]
timestamp: 2026-07-28T00:00:00Z
---

# Partners

## Business Definition

The Partners entity represents the dimension table that stores information about direct and indirect sales partners involved in fulfilling customer bookings. Each record contains partner identity attributes, partner type classifications, partner tier designations, and route-to-market categorizations. This entity enables analysis of booking transactions by partner characteristics and supports channel strategy optimization.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_partner

**Source Schema**: quotetobooking

**Entity Type**: Dimension Table

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

None

---

## Relationships

- [Bookings to Partners](../relationships/bookings-to-partners.md)

---

## Measures

All booking-related measures can be analyzed by partner attributes:
- [Booking Count](../measures/booking-count.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Average Discount Percentage](../measures/average-discount-pct.md)

---

## Related Concepts

- [Partner Type](../glossary/partner-type.md)
- [Route to Market](../glossary/route-to-market.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

1. **Unique Partner Key**: Each partner record must have a unique partner_key
2. **Partner Identifier**: partner_id represents the business identifier for the partner organization
3. **Partner Type Classification**: Partners are classified by type such as distributor, reseller, systems integrator, or direct channel
4. **Partner Tier Designation**: Partners are assigned program tiers or status levels
5. **Route to Market**: Each partner is associated with a sales channel path through which products are sold

---

## Attribute Definitions

### partner_key
Surrogate key that uniquely identifies a partner record in the partner dimension. Used as the primary key and referenced by the bookings fact table.

### partner_id
Business identifier assigned to the partner organization. Represents the natural key used in operational systems.

### partner_name
Official name of the partner organization. Used for reporting and partner identification.

### partner_type
Classification of the partner, such as distributor, reseller, systems integrator, or direct channel. Enables partner type analysis and channel strategy evaluation.

### partner_tier
Program tier or status level assigned to the partner. Used to track partner program participation and performance by tier.

### route_to_market
Sales channel path through which the product or service is sold to the customer. Enables route-to-market analysis and channel optimization.

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Usage Examples

### Partner Type Analysis
- Analyze booking amount by partner type
- Compare direct vs indirect channel performance
- Track distributor vs reseller effectiveness

### Partner Tier Analysis
- Evaluate partner performance by tier level
- Track tier progression and partner development
- Identify top-performing partner tiers

### Route to Market Analysis
- Analyze revenue distribution by sales channel
- Optimize channel mix and strategy
- Identify most effective routes to market

### Partner Performance Analysis
- Rank partners by booking amount
- Track partner contribution to revenue
- Identify strategic partner relationships

---

## Data Quality Checks

- partner_key is unique and not null
- partner_id is not null
- partner_name is not null
- partner_type is a valid type classification
- partner_tier is a valid tier designation
- route_to_market is a valid channel path
