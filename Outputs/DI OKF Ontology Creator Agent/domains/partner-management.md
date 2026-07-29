---
title: Partner Management Domain
type: domain
description: Channel partner master data used to analyze bookings by partner identity, type, tier, and route to market
resource: domains
tags: [okf, domain, partner-management, partner, channel]
timestamp: 2026-07-28T00:00:00Z
---

# Partner Management Domain

## Business Definition

The Partner Management domain encompasses channel partner master data used to analyze bookings by partner identity, type, tier, and route to market. This domain provides the partner dimensional context necessary for channel sales analytics.

---

## Business Purpose

This domain enables business users to:

- Analyze sales performance by channel partner
- Track revenue by partner type and tier
- Evaluate route to market effectiveness
- Monitor partner program performance
- Identify top performing partners
- Measure channel contribution
- Support partner relationship management

---

## Domain Scope

### Included
- Partner identity and identification
- Partner type classifications
- Partner tier and certification levels
- Route to market categorizations
- Partner descriptive attributes

### Excluded
- Partner contact information
- Partner agreements and contracts
- Partner commissions and incentives
- Partner training and certification details
- Partner performance scorecards

---

## Related Entities

### Primary Entities
- [Partner Dimension](../entities/partner-dimension.md)

---

## Related Measures

All sales and revenue measures can be analyzed by partner attributes:

- [Quantity Sold](../measures/quantity-sold.md) by partner
- [Booking Amount USD](../measures/booking-amount-usd.md) by partner
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md) by partner
- [Total Contract Value USD](../measures/total-contract-value-usd.md) by partner
- [Unit List Price USD](../measures/unit-list-price-usd.md) by partner
- [Discount Percentage](../measures/discount-percentage.md) by partner

---

## Related Relationships

- [Partner to Booking](../relationships/partner-to-booking.md)

---

## Key Business Concepts

### Partner Type
Classification of the partner organization such as:
- **Distributor**: Wholesale distribution partners
- **Value-Added Reseller (VAR)**: Resellers providing additional services
- **Systems Integrator**: Partners providing integration and implementation services
- **Direct**: Direct sales without partner involvement

### Partner Tier
Tier or certification level assigned to the partner in the channel program, reflecting:
- Partner capabilities and certifications
- Partner investment and commitment
- Partner performance and revenue contribution
- Partner benefits and incentives eligibility

### Route to Market
Sales route through which the booking was transacted:
- **Direct**: Direct sales to end customer
- **Reseller**: Single-tier channel through reseller
- **Two-Tier**: Distribution through distributor to reseller
- **Marketplace**: Cloud marketplace transactions

---

## Business Rules

1. Every partner must have a unique Partner Key (surrogate key)
2. Every partner must have a unique Partner ID (business key)
3. Partner Name is required for reporting and analysis
4. Partner Type must match approved partner type classifications
5. Partner Tier should reflect current certification level
6. Route to Market must align with partner type
7. Direct sales may have a special "Direct" partner record

---

## Analytical Use Cases

### Partner Performance Analysis
- Track revenue and bookings by partner
- Identify top performing partners
- Analyze partner growth trends
- Monitor partner contribution to total revenue

### Partner Type Analysis
- Compare performance across partner types
- Analyze channel mix and trends
- Identify optimal partner types by customer segment or product
- Track partner type profitability

### Partner Tier Analysis
- Compare performance across partner tiers
- Analyze tier program effectiveness
- Track tier progression and partner development
- Evaluate tier-based incentive programs

### Route to Market Analysis
- Analyze revenue by route to market
- Compare direct versus channel performance
- Evaluate two-tier versus single-tier effectiveness
- Optimize channel strategy and coverage

### Partner Segmentation
- Segment partners by performance, tier, and type
- Identify strategic partners for investment
- Target partner recruitment and development
- Support partner account planning

---

## Data Quality Metrics

### Completeness
- Partner Key must be populated for all records
- Partner ID must be populated for all records
- Partner Name must be populated for all records
- Partner Type should be populated (>95% target)
- Route to Market should be populated (>95% target)

### Accuracy
- Partner ID must be unique
- Partner Type must match approved type values
- Partner Tier must match approved tier values
- Route to Market must match approved route values
- Partner attributes must align with partner program rules

### Consistency
- Route to Market must align with Partner Type
- Partner attributes must be consistent across all bookings
- Partner master data must reconcile with source partner systems

---

## Technical Implementation

### Source System
- **Schema**: quotetobooking
- **Table**: dim_partner
- **Primary Key**: partner_key (surrogate key)
- **Business Key**: partner_id
- **Type**: Slowly Changing Dimension (Type 1 or Type 2)

### Key Attributes
- Partner Key (Primary Key)
- Partner ID (Business Key)
- Partner Name
- Partner Type
- Partner Tier
- Route to Market

---

## Semantic Links

### Related Domains
- [Sales Transactions](sales-transactions.md)
- [Customer Management](customer-management.md)
- [Product Management](product-management.md)
- [Geography](geography.md)

### Related Glossary Terms
- [Partner Dimension](../glossary/partner-dimension.md)
- [Partner Key](../glossary/partner-key.md)
- [Partner ID](../glossary/partner-id.md)
- [Partner Name](../glossary/partner-name.md)
- [Partner Type](../glossary/partner-type.md)
- [Partner Tier](../glossary/partner-tier.md)
- [Route to Market](../glossary/route-to-market.md)

---

## Navigation

- [Back to Domains Index](index.md)
- [Back to Bundle Index](../index.md)
