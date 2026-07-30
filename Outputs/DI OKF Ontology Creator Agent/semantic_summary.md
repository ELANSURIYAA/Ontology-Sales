---
title: Semantic Summary
type: index
description: High-level semantic model overview and architecture summary
resource: knowledge_bundle
tags: [semantic, summary, model, architecture, overview]
timestamp: 2024-01-15T00:00:00Z
---

# Semantic Summary

## Model Overview

**Model Name**: sales_bookings_and_revenue_analytics  
**Version**: 0.1  
**Purpose**: Sales bookings and revenue analytics semantic model for completed booking transactions

---

## Business Context

This semantic model supports sales booking and revenue analysis. Booking transactions are represented at the booking transaction grain in the bookings dataset. Use booking date for time-based analysis and the defined metrics for booking amount, ACV, TCV, quantity, discount, renewal, and order analysis.

---

## Semantic Architecture

### Core Fact
- **Bookings** - Individual completed sales booking transactions with financial measures, quantities, renewal status, and dimensional links

### Dimensions

#### Customer Dimension
- Customer identity, segment, industry, account tier, and headquarters location

#### Product Dimension
- Product identity, family, technology domain, offer type, and business entity

#### Partner Dimension
- Partner identity, type, tier, and route to market

#### Geography Dimension
- Geographic sales territories by region, theater, and country

#### Sales Representative Dimension
- Sales person identity, role, team, and segment coverage

#### Contract Dimension
- Commercial agreement terms including type, duration, renewal behavior, and coverage level

#### Date Dimension
- Calendar and fiscal time attributes for reporting periods, years, quarters, and months

---

## Data Model Pattern

**Pattern**: Star Schema  
**Grain**: Individual booking transaction  
**Fact Table**: bookings  
**Dimension Tables**: 7

---

## Relationship Summary

All relationships follow a **many-to-one** pattern from the bookings fact table to dimension tables:

1. Bookings → Contracts
2. Bookings → Customers
3. Bookings → Dates
4. Bookings → Geographies
5. Bookings → Partners
6. Bookings → Products
7. Bookings → Sales Representatives

---

## Measure Categories

### Volume Metrics
- Booking Count
- Distinct Order Count
- Total Quantity

### Revenue Metrics
- Total Booking Amount USD
- Total ACV USD
- Total TCV USD
- Renewal Booking Amount USD
- Net New Booking Amount USD

### Average Metrics
- Average Discount Percentage
- Average Selling Price USD
- Average Booking Value USD

---

## Key Business Concepts

### Booking Transaction
The atomic unit of analysis representing a completed sales booking with associated financial measures and dimensional context.

### Annual Contract Value (ACV)
Annualized contract value of the booking in US dollars, used for subscription and recurring revenue analysis.

### Total Contract Value (TCV)
Total contract value over the full contract term in US dollars, used for multi-year deal analysis.

### Renewal vs Net New
Bookings are classified as either renewal transactions (existing customer contract renewals) or net new business (new customer acquisitions or expansions).

---

## Source Systems

**Primary Source**: quotetobooking schema

### Source Tables
- quotetobooking.fact_bookings
- quotetobooking.dim_customer
- quotetobooking.dim_product
- quotetobooking.dim_partner
- quotetobooking.dim_geography
- quotetobooking.dim_sales_rep
- quotetobooking.dim_contract
- quotetobooking.dim_date

---

## Semantic Completeness

| Component | Count | Status |
|-----------|-------|--------|
| Domains | 8 | ✓ Complete |
| Entities | 8 | ✓ Complete |
| Relationships | 7 | ✓ Complete |
| Measures | 11 | ✓ Complete |
| Glossary Terms | 50+ | ✓ Complete |

---

## Navigation

- [Return to Index](index.md)
- [View All Domains](domains/index.md)
- [View All Entities](entities/index.md)
- [View All Relationships](relationships/index.md)
- [View All Measures](measures/index.md)
- [View Glossary](glossary/index.md)
- [View Metrics Summary](metrics.md)
