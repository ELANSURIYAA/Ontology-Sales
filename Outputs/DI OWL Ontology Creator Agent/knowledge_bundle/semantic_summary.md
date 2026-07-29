---
title: Semantic Summary
type: index
description: High-level overview of the Sales Bookings and Revenue Analytics semantic model
resource: knowledge_bundle
tags: [semantic, summary, overview, model, sales, bookings]
timestamp: 2026-07-28T00:00:00Z
---

# Semantic Summary

## Business Context

The Sales Bookings and Revenue Analytics semantic model represents enterprise sales booking operations for networking, security, collaboration, observability, and software subscription products. The model captures completed customer bookings and enables comprehensive analysis of sales performance across multiple business dimensions.

---

## Domain Overview

### Sales Bookings and Revenue Analytics

This domain encompasses all aspects of sales booking operations including:

- Customer relationship management
- Product and offer management
- Partner and channel operations
- Geographic sales coverage
- Contract and agreement tracking
- Sales representative performance
- Revenue and financial metrics

The domain supports strategic decision-making through dimensional analysis of booking transactions across time, geography, customer segments, product portfolios, and sales channels.

---

## Entity Architecture

### Dimensional Entities

The model follows a dimensional architecture with seven dimension entities providing business context:

1. **[Contract](./entities/contract.md)** - Commercial agreements and terms
2. **[Customer](./entities/customer.md)** - Customer organizations and accounts
3. **[Date](./entities/date.md)** - Calendar and fiscal time periods
4. **[Geography](./entities/geography.md)** - Sales regions and territories
5. **[Partner](./entities/partner.md)** - Channel and direct partners
6. **[Product](./entities/product.md)** - Products and subscription offers
7. **[Sales Representative](./entities/sales-representative.md)** - Sales personnel

### Fact Entity

1. **[Booking Transaction](./entities/booking-transaction.md)** - Individual sales booking records with financial measures

---

## Relationship Model

The semantic model implements a star schema pattern with the Booking Transaction fact entity at the center, connected to seven dimension entities through foreign key relationships:

- Contract → Booking Transaction (One-to-Many)
- Customer → Booking Transaction (One-to-Many)
- Date → Booking Transaction (One-to-Many)
- Geography → Booking Transaction (One-to-Many)
- Partner → Booking Transaction (One-to-Many)
- Product → Booking Transaction (One-to-Many)
- Sales Representative → Booking Transaction (One-to-Many)

All relationships are validated with 1.00 confidence scores, ensuring data integrity and referential consistency.

---

## Measure Framework

The model includes six core financial measures supporting revenue analytics:

1. **[Quantity Sold](./measures/quantity-sold.md)** - Units, licenses, or subscriptions
2. **[Unit List Price USD](./measures/unit-list-price-usd.md)** - Standard pricing
3. **[Discount Percentage](./measures/discount-percentage.md)** - Price adjustments
4. **[Booking Amount USD](./measures/booking-amount-usd.md)** - Total booked revenue
5. **[Annual Contract Value USD](./measures/annual-contract-value-usd.md)** - Annualized contract value
6. **[Total Contract Value USD](./measures/total-contract-value-usd.md)** - Full contract value

These measures enable comprehensive financial analysis including revenue recognition, pricing analysis, discount management, and contract value tracking.

---

## Business Glossary

The model includes 69 standardized business terms covering:

- Entity definitions
- Attribute definitions
- Business keys and identifiers
- Dimensional attributes
- Measure definitions
- Technical mappings

All glossary terms are mapped to technical implementations with confidence scores, ensuring semantic consistency between business and technical layers.

---

## Technical Architecture

### Source System

**Database**: QuoteToBooking  
**Schema**: Dimensional star schema  
**Tables**: 8 (7 dimensions + 1 fact)

### Data Model Pattern

- **Type**: Star Schema
- **Grain**: Individual booking transaction
- **Keys**: Surrogate keys for dimensions, composite business keys for fact
- **Slowly Changing Dimensions**: Type 1 (overwrite)

### Integration Points

The model supports integration with:
- Business intelligence platforms
- Data warehouses
- Analytics applications
- Reporting systems
- Ontology frameworks

---

## Analytical Capabilities

### Dimensional Analysis

- **Time**: Calendar and fiscal period analysis
- **Geography**: Region, theater, and country analysis
- **Customer**: Segment, industry, and account tier analysis
- **Product**: Family, technology domain, and offer type analysis
- **Partner**: Type, tier, and route-to-market analysis
- **Contract**: Type, term, and coverage analysis
- **Sales**: Representative, role, and team analysis

### Measure Analysis

- Revenue and booking analysis
- Contract value tracking
- Pricing and discount analysis
- Volume and quantity analysis
- Performance trending
- Comparative analysis

---

## Semantic Links

- [Complete Domain Catalog](./domains/index.md)
- [Complete Entity Catalog](./entities/index.md)
- [Complete Relationship Catalog](./relationships/index.md)
- [Complete Measure Catalog](./measures/index.md)
- [Complete Business Glossary](./glossary/index.md)
- [Metrics Overview](./metrics.md)

---

## Model Statistics

| Component | Count |
|-----------|-------|
| Business Domains | 1 |
| Business Entities | 8 |
| Business Attributes | 61 |
| Semantic Relationships | 7 |
| Business Measures | 6 |
| Glossary Terms | 69 |
| Primary Keys | 8 |
| Foreign Keys | 7 |

---

## Metadata

**Model Name**: Sales Bookings and Revenue Analytics  
**Model Type**: Dimensional Star Schema  
**Source**: OSI Semantic Model  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
