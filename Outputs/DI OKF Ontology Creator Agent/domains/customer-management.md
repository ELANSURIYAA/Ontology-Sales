---
title: Customer Management Domain
type: domain
description: Customer master data used to analyze bookings by customer identity, segment, industry, and location
resource: domains
tags: [okf, domain, customer-management, customer, segmentation]
timestamp: 2026-07-28T00:00:00Z
---

# Customer Management Domain

## Business Definition

The Customer Management domain encompasses customer master data used to analyze bookings by customer identity, segment, industry, account tier, and headquarters location. This domain provides the customer dimensional context necessary for customer-centric sales analytics.

---

## Business Purpose

This domain enables business users to:

- Analyze sales performance by customer segment
- Track revenue by industry vertical
- Evaluate account tier profitability
- Monitor geographic customer distribution
- Identify strategic customer relationships
- Segment customers for targeted analysis
- Measure customer lifetime value and contribution

---

## Domain Scope

### Included
- Customer identity and identification
- Customer segmentation attributes
- Industry classifications
- Account tier and strategic importance
- Headquarters location (country and region)
- Customer descriptive attributes

### Excluded
- Customer contact information
- Customer billing and payment data
- Customer relationship history
- Customer satisfaction metrics
- Customer support tickets

---

## Related Entities

### Primary Entities
- [Customer Dimension](../entities/customer-dimension.md)

---

## Related Measures

All sales and revenue measures can be analyzed by customer attributes:

- [Quantity Sold](../measures/quantity-sold.md) by customer
- [Booking Amount USD](../measures/booking-amount-usd.md) by customer
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md) by customer
- [Total Contract Value USD](../measures/total-contract-value-usd.md) by customer
- [Unit List Price USD](../measures/unit-list-price-usd.md) by customer
- [Discount Percentage](../measures/discount-percentage.md) by customer

---

## Related Relationships

- [Customer to Booking](../relationships/customer-to-booking.md)

---

## Key Business Concepts

### Customer Segmentation
Customers are classified into market segments based on size, business model, and strategic importance:
- **Enterprise**: Large organizations with complex needs
- **Service Provider**: Telecommunications and service providers
- **Public Sector**: Government and educational institutions
- **Commercial**: Mid-market and small business customers

### Industry Classification
Customers are categorized by industry vertical to enable industry-specific analysis and benchmarking.

### Account Tier
Strategic importance classification that reflects customer relationship value, potential, and engagement level.

### Headquarters Location
Geographic location of customer headquarters used for regional analysis and territory management.

---

## Business Rules

1. Every customer must have a unique Customer Key (surrogate key)
2. Every customer must have a unique Customer ID (business key)
3. Customer Name is required for reporting and analysis
4. Customer Segment should be populated for all customers
5. Headquarters Country and Region should align with standard geographic hierarchies
6. Account Tier should reflect current strategic classification

---

## Analytical Use Cases

### Customer Segmentation Analysis
- Compare revenue and booking performance across customer segments
- Analyze product adoption by segment
- Identify segment-specific pricing and discount patterns
- Track segment growth and market share

### Industry Vertical Analysis
- Benchmark performance across industry verticals
- Identify industry-specific product preferences
- Analyze industry trends and seasonality
- Target industry-specific sales strategies

### Account Management
- Identify top customers by revenue contribution
- Track strategic account performance
- Monitor account tier distribution
- Analyze customer concentration risk

### Geographic Customer Analysis
- Analyze customer distribution by region and country
- Compare performance across customer geographies
- Identify expansion opportunities
- Support territory planning and coverage

---

## Data Quality Metrics

### Completeness
- Customer Key must be populated for all records
- Customer ID must be populated for all records
- Customer Name must be populated for all records
- Customer Segment should be populated (>95% target)

### Accuracy
- Customer ID must be unique
- Headquarters Country must match standard country codes
- Customer Segment must match approved segment values
- Account Tier must match approved tier classifications

### Consistency
- Headquarters Region must align with Headquarters Country
- Customer attributes must be consistent across all bookings
- Customer master data must reconcile with source CRM systems

---

## Technical Implementation

### Source System
- **Schema**: quotetobooking
- **Table**: dim_customer
- **Primary Key**: customer_key (surrogate key)
- **Business Key**: customer_id
- **Type**: Slowly Changing Dimension (Type 1 or Type 2)

### Key Attributes
- Customer Key (Primary Key)
- Customer ID (Business Key)
- Customer Name
- Customer Segment
- Industry
- Account Tier
- Headquarters Country
- Headquarters Region

---

## Semantic Links

### Related Domains
- [Sales Transactions](sales-transactions.md)
- [Geography](geography.md)
- [Sales Organization](sales-organization.md)
- [Contract Management](contract-management.md)

### Related Glossary Terms
- [Customer Dimension](../glossary/customer-dimension.md)
- [Customer Key](../glossary/customer-key.md)
- [Customer ID](../glossary/customer-id.md)
- [Customer Name](../glossary/customer-name.md)
- [Customer Segment](../glossary/customer-segment.md)
- [Industry](../glossary/industry.md)
- [Account Tier](../glossary/account-tier.md)
- [Headquarters Country](../glossary/headquarters-country.md)
- [Headquarters Region](../glossary/headquarters-region.md)

---

## Navigation

- [Back to Domains Index](index.md)
- [Back to Bundle Index](../index.md)
