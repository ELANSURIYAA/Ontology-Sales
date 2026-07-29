---
title: Semantic Summary
type: index
description: High-level overview of the Quote to Booking semantic model
resource: knowledge_bundle
tags: [okf, semantic-model, summary, quote-to-booking]
timestamp: 2026-07-28T00:00:00Z
---

# Semantic Summary

## Overview

The Quote to Booking semantic model represents a comprehensive enterprise sales analytics framework designed to track, measure, and analyze booking transactions across multiple business dimensions. This model supports strategic decision-making for sales performance, revenue recognition, customer segmentation, product portfolio analysis, and channel partner management.

---

## Business Context

The Quote to Booking process captures the complete lifecycle of sales transactions from customer quotation through final booking confirmation. This semantic model enables business users to analyze sales performance across:

- Customer segments and industries
- Product families and technology domains
- Geographic regions and theaters
- Channel partners and routes to market
- Sales representatives and teams
- Contract types and terms
- Time periods and fiscal calendars

---

## Domain Architecture

The semantic model is organized into **10 business domains**:

### Transactional Domains
- **Sales Transactions**: Core booking events and sales performance measures
- **Contract Management**: Commercial agreements and service terms

### Master Data Domains
- **Customer Management**: Customer identity, segmentation, and classification
- **Product Management**: Product catalog, families, and technology domains
- **Partner Management**: Channel partners, types, and tiers
- **Geography**: Regional, theater, and country hierarchies
- **Sales Organization**: Sales representatives, roles, and teams

### Analytical Domains
- **Time Management**: Calendar and fiscal time dimensions
- **Pricing**: List prices and discount structures
- **Revenue Metrics**: Financial value measures and contract values

---

## Entity Model

The semantic model contains **8 core entities**:

### Dimension Entities (7)
1. **Contract Dimension**: Contract attributes and service agreements
2. **Customer Dimension**: Customer master data and segmentation
3. **Date Dimension**: Calendar and fiscal time attributes
4. **Geography Dimension**: Geographic hierarchies
5. **Partner Dimension**: Channel partner master data
6. **Product Dimension**: Product catalog and classifications
7. **Sales Representative Dimension**: Sales organization attributes

### Fact Entities (1)
8. **Booking Fact**: Transactional booking records with measures

---

## Relationship Model

The model implements a **star schema** with **7 foreign key relationships** connecting dimension entities to the central Booking Fact:

- Contract Dimension → Booking Fact
- Customer Dimension → Booking Fact
- Date Dimension → Booking Fact
- Geography Dimension → Booking Fact
- Partner Dimension → Booking Fact
- Product Dimension → Booking Fact
- Sales Representative Dimension → Booking Fact

All relationships follow a **one-to-many** cardinality pattern, enabling efficient aggregation and drill-down analysis.

---

## Measure Framework

The model defines **6 core business measures**:

### Volume Measures
- **Quantity Sold**: Units, licenses, or subscriptions booked

### Pricing Measures
- **Unit List Price USD**: Standard list price per unit
- **Discount Percentage**: Applied discount rate

### Revenue Measures
- **Booking Amount USD**: Total booked revenue
- **Annual Contract Value USD**: Annualized recurring revenue
- **Total Contract Value USD**: Full contract term value

---

## Attribute Coverage

The semantic model contains **61 business attributes** distributed across entities:

- **Contract Dimension**: 5 attributes
- **Customer Dimension**: 8 attributes
- **Date Dimension**: 7 attributes
- **Geography Dimension**: 4 attributes
- **Partner Dimension**: 6 attributes
- **Product Dimension**: 7 attributes
- **Sales Representative Dimension**: 6 attributes
- **Booking Fact**: 18 attributes (including 7 foreign keys and 6 measures)

---

## Glossary Coverage

The business glossary contains **72 standardized terms** with complete business definitions and technical mappings, ensuring consistent terminology across:

- Entity definitions
- Attribute definitions
- Measure definitions
- Relationship definitions
- Business rules
- Technical implementations

---

## Technical Implementation

### Source System
- **Database Schema**: quotetobooking
- **Fact Table**: fact_bookings
- **Dimension Tables**: 7 dimension tables (dim_contract, dim_customer, dim_date, dim_geography, dim_partner, dim_product, dim_sales_rep)

### Data Model Pattern
- **Architecture**: Star Schema
- **Grain**: Individual booking transaction line
- **Primary Keys**: Surrogate keys on all dimensions
- **Foreign Keys**: 7 dimensional references in fact table

---

## Analytical Capabilities

This semantic model enables analysis across multiple perspectives:

### Customer Analytics
- Customer segmentation analysis
- Industry vertical performance
- Account tier profitability
- Geographic customer distribution

### Product Analytics
- Product family performance
- Technology domain trends
- Offer type mix analysis
- Business entity contribution

### Sales Analytics
- Sales representative performance
- Team productivity metrics
- Segment coverage analysis
- Booking type distribution

### Partner Analytics
- Partner type performance
- Partner tier analysis
- Route to market effectiveness
- Channel contribution

### Financial Analytics
- Booking revenue trends
- Annual contract value analysis
- Total contract value tracking
- Discount and pricing analysis

### Time Analytics
- Fiscal period performance
- Year-over-year comparisons
- Quarterly trends
- Monthly booking patterns

---

## Semantic Completeness

✓ All domains documented  
✓ All entities documented  
✓ All attributes documented  
✓ All relationships documented  
✓ All measures documented  
✓ All glossary terms documented  
✓ Business definitions complete  
✓ Technical mappings complete  
✓ Semantic cross-links established  
✓ Metadata validated  

---

## Related Resources

- [Complete Domain Catalog](domains/index.md)
- [Complete Entity Catalog](entities/index.md)
- [Complete Relationship Catalog](relationships/index.md)
- [Complete Measure Catalog](measures/index.md)
- [Complete Business Glossary](glossary/index.md)
- [Metrics Overview](metrics.md)
