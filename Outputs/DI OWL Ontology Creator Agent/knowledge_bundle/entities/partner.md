---
title: Partner
type: entity
description: Channel and direct partners involved in the sales process including partner type, partner tier, and route to market
resource: entities
tags: [partner, channel, reseller, dimension, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Partner

## Business Definition

The Partner entity stores information about channel and direct partners involved in the sales process. It captures partner characteristics including partner type, partner tier, and route to market. This entity enables analysis of channel performance, partner contribution, and route-to-market effectiveness.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_partner  
**Source Schema**: QuoteToBooking  
**Entity Type**: Dimension  
**Entity ID**: ENT005

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

- **Partner Key** (partner_key) - Surrogate key, Integer, Not Nullable

---

## Foreign Keys

None - This is a dimension entity

---

## Relationships

### Outgoing Relationships

- **[Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)** - One-to-Many relationship linking partners to booking transactions

### Related Entities

- **[Booking Transaction](./booking-transaction.md)** - Fact entity containing booking records with partner involvement
- **[Customer](./customer.md)** - Customers served through partners
- **[Product](./product.md)** - Products sold through partner channels
- **[Geography](./geography.md)** - Geographic markets served by partners

---

## Measures

Partners support channel analysis of all measures:

- **[Booking Amount USD](../measures/booking-amount-usd.md)** - Revenue by partner and channel
- **[Annual Contract Value USD](../measures/annual-contract-value-usd.md)** - ACV by partner type
- **[Total Contract Value USD](../measures/total-contract-value-usd.md)** - TCV by partner tier
- **[Quantity Sold](../measures/quantity-sold.md)** - Volume by route to market
- **[Discount Percentage](../measures/discount-percentage.md)** - Channel pricing patterns
- **[Unit List Price USD](../measures/unit-list-price-usd.md)** - Partner pricing strategies

---

## Business Rules

1. Partner Key must be unique and not null
2. Partner ID must be unique and not null
3. Partner Name is required for all partner records
4. Partner Type must be from approved list (Distributor, Reseller, Systems Integrator, Direct, etc.)
5. Partner Tier must be from approved tier classification (Gold, Silver, Bronze, Authorized, etc.)
6. Route to Market must be from approved list (Direct, Two-Tier, One-Tier, etc.)
7. Direct sales must have Partner Type = 'Direct'

---

## Analytical Usage

### Partner Type Analysis
- Compare booking performance across distributors, resellers, and systems integrators
- Analyze direct vs indirect channel mix
- Track channel type trends and shifts

### Partner Tier Analysis
- Evaluate performance by partner certification level
- Compare Gold, Silver, and Bronze partner contribution
- Track partner tier progression and upgrades

### Route to Market Analysis
- Analyze booking distribution by sales delivery path
- Compare direct vs two-tier vs one-tier performance
- Optimize route-to-market strategy

### Partner Performance
- Identify top-performing partners
- Track partner growth and contribution
- Analyze partner specialization and focus areas

---

## Partner Hierarchy

```
Route to Market
  └─ Partner Type
      └─ Partner Tier
          └─ Partner Name
```

### Example Classifications

**Partner Types**:
- Distributor
- Reseller
- Systems Integrator
- Managed Service Provider
- Direct

**Partner Tiers**:
- Gold Partner
- Silver Partner
- Bronze Partner
- Authorized Partner
- Strategic Partner

**Route to Market**:
- Direct
- One-Tier (Direct to Partner to Customer)
- Two-Tier (Direct to Distributor to Reseller to Customer)

---

## Related Concepts

- **[Customer](./customer.md)** - Customers served by partners
- **[Product](./product.md)** - Products distributed through channels
- **[Geography](./geography.md)** - Partner geographic coverage
- **[Sales Representative](./sales-representative.md)** - Partner relationship managers
- **[Booking Transaction](./booking-transaction.md)** - Partner-involved transactions

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

## Attribute Details

| Attribute | Technical Column | Data Type | Nullable | Key Type | Description |
|-----------|-----------------|-----------|----------|----------|-------------|
| Partner Key | partner_key | integer | No | Primary | Surrogate key uniquely identifying partner |
| Partner ID | partner_id | character varying(20) | No | Business | Business identifier for partner organization |
| Partner Name | partner_name | character varying(60) | Yes | - | Name of partner organization |
| Partner Type | partner_type | character varying(30) | Yes | - | Partner operating model classification |
| Partner Tier | partner_tier | character varying(30) | Yes | - | Partner certification or tier level |
| Route to Market | route_to_market | character varying(20) | Yes | - | Sales delivery path designation |

---

## Semantic Links

- [Entity Index](./index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Relationship Index](../relationships/index.md)
- [Measure Index](../measures/index.md)
- [Main Index](../index.md)

---

## Metadata

**Entity ID**: ENT005  
**Domain ID**: DOM001  
**Entity Type**: Dimension  
**Technical Table**: QuoteToBooking.dim_partner  
**Total Attributes**: 6  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
