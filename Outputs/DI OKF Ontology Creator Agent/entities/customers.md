---
title: Customers
type: entity
description: Stores descriptive information about customers that place orders, including identity, segment, industry, account tier, and headquarters location
resource: entities
tags: [customers, dimension, customer-segment, industry]
timestamp: 2026-07-28T00:00:00Z
---

# Customers

## Business Definition

The Customers entity represents the dimension table that stores descriptive information about customer organizations that place orders. Each record contains customer identity attributes, market segment classification, industry categorization, account tier designation, and headquarters location information. This entity enables analysis of booking transactions by customer characteristics and supports customer segmentation strategies.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_customer

**Source Schema**: quotetobooking

**Entity Type**: Dimension Table

---

## Attributes

- customer_key
- customer_id
- customer_name
- segment
- industry
- account_tier
- hq_country
- hq_region

---

## Primary Keys

- customer_key

---

## Foreign Keys

None

---

## Relationships

- [Bookings to Customers](../relationships/bookings-to-customers.md)

---

## Measures

All booking-related measures can be analyzed by customer attributes:
- [Booking Count](../measures/booking-count.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

---

## Related Concepts

- [Customer Segment](../glossary/customer-segment.md)
- [Booking Transaction](../glossary/booking-transaction.md)
- [Geography Region](../glossary/geography-region.md)

---

## Business Rules

1. **Unique Customer Key**: Each customer record must have a unique customer_key
2. **Customer Identifier**: customer_id represents the business identifier for the customer account
3. **Segment Classification**: Customers are classified into market segments such as Enterprise, Service Provider, or Public Sector
4. **Industry Classification**: Customers are categorized by industry vertical
5. **Account Tier**: Strategic importance or service tier is assigned to each customer account
6. **Headquarters Location**: Customer headquarters location is captured at country and region levels

---

## Attribute Definitions

### customer_key
Surrogate key that uniquely identifies a customer record in the customer dimension. Used as the primary key and referenced by the bookings fact table.

### customer_id
Business identifier assigned to the customer account. Represents the natural key used in operational systems.

### customer_name
Official name of the customer organization. Used for reporting and customer identification.

### segment
Market segment the customer belongs to, such as Enterprise, Service Provider, or Public Sector. Used for customer segmentation and targeted analysis.

### industry
Industry classification of the customer organization. Enables industry-specific analysis and benchmarking.

### account_tier
Strategic importance or service tier assigned to the customer account. Used to prioritize customer relationships and allocate resources.

### hq_country
Country where the customer organization's headquarters is located. Enables geographic analysis of customer base.

### hq_region
Broad geographic region of the customer organization's headquarters. Provides high-level geographic grouping for analysis.

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Usage Examples

### Customer Segmentation Analysis
- Analyze booking amount by customer segment
- Compare Enterprise vs Service Provider performance
- Track Public Sector booking trends

### Industry Analysis
- Identify top-performing industries by revenue
- Analyze industry-specific booking patterns
- Benchmark performance across industries

### Account Tier Analysis
- Track booking concentration by account tier
- Identify strategic account performance
- Prioritize customer engagement strategies

### Geographic Analysis
- Analyze customer distribution by headquarters region
- Track booking performance by customer location
- Identify geographic expansion opportunities

---

## Data Quality Checks

- customer_key is unique and not null
- customer_id is not null
- customer_name is not null
- segment is a valid segment value
- industry is a valid industry classification
- account_tier is a valid tier designation
- hq_country is a valid country code
- hq_region is a valid region designation
