---
title: Customer
type: entity
description: Customer organizations that place orders and generate bookings including segment, industry, account tier, and headquarters location
resource: entities
tags: [customer, account, dimension, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Customer

## Business Definition

The Customer entity stores descriptive information about customers that place orders and generate bookings. It captures customer organizational characteristics including customer segment, industry classification, account tier, and headquarters location. This entity enables comprehensive customer analysis and segmentation for sales performance tracking and strategic account management.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer  
**Source Schema**: QuoteToBooking  
**Entity Type**: Dimension  
**Entity ID**: ENT002

---

## Attributes

- **Customer Key** - Surrogate key that uniquely identifies a customer record in the customer dimension
- **Customer ID** - Business identifier assigned to the customer account
- **Customer Name** - Official name of the customer organization that purchased products or services
- **Customer Segment** - Classifies the customer into a business segment such as Enterprise, Service Provider, or Public Sector
- **Industry** - Identifies the industry in which the customer operates
- **Account Tier** - Indicates the strategic importance or service tier of the customer account
- **Headquarters Country** - Country where the customer organization's headquarters is located
- **Headquarters Region** - Global region where the customer organization's headquarters is located

---

## Primary Keys

- **Customer Key** (customer_key) - Surrogate key, Integer, Not Nullable

---

## Foreign Keys

None - This is a dimension entity

---

## Relationships

### Outgoing Relationships

- **[Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)** - One-to-Many relationship linking customers to booking transactions

### Related Entities

- **[Booking Transaction](./booking-transaction.md)** - Fact entity containing booking records for customers
- **[Geography](./geography.md)** - Geographic locations where customers operate
- **[Sales Representative](./sales-representative.md)** - Sales personnel managing customer relationships

---

## Measures

Customers support analysis of the following measures:

- **[Booking Amount USD](../measures/booking-amount-usd.md)** - Total revenue by customer and segment
- **[Annual Contract Value USD](../measures/annual-contract-value-usd.md)** - ACV by customer characteristics
- **[Total Contract Value USD](../measures/total-contract-value-usd.md)** - TCV by customer attributes
- **[Quantity Sold](../measures/quantity-sold.md)** - Volume by customer segment
- **[Discount Percentage](../measures/discount-percentage.md)** - Pricing by customer tier

---

## Business Rules

1. Customer Key must be unique and not null
2. Customer ID must be unique and not null
3. Customer Name is required for all customer records
4. Customer Segment must be from approved list (Enterprise, Service Provider, Public Sector, etc.)
5. Account Tier must be from approved tier classification
6. Headquarters Country must be valid ISO country code
7. Headquarters Region must align with country location

---

## Analytical Usage

### Customer Segment Analysis
- Compare booking performance across Enterprise, Service Provider, and Public Sector segments
- Analyze segment mix and trends over time
- Evaluate revenue contribution by customer segment

### Industry Analysis
- Track booking performance by industry vertical
- Identify high-performing industries
- Analyze industry-specific product preferences

### Account Tier Analysis
- Monitor strategic account performance
- Compare tier-based booking patterns
- Track account tier migration and growth

### Geographic Analysis
- Analyze customer distribution by headquarters location
- Compare regional customer characteristics
- Track international vs domestic customer mix

---

## Related Concepts

- **[Geography](./geography.md)** - Sales territories and customer locations
- **[Product](./product.md)** - Products purchased by customers
- **[Contract](./contract.md)** - Agreements with customers
- **[Sales Representative](./sales-representative.md)** - Account management relationships
- **[Partner](./partner.md)** - Channel partners serving customers
- **[Booking Transaction](./booking-transaction.md)** - Customer purchase transactions

---

## Glossary Terms

- [Customer](../glossary/customer.md)
- [Customer Key](../glossary/customer-key.md)
- [Customer ID](../glossary/customer-id.md)
- [Customer Name](../glossary/customer-name.md)
- [Customer Segment](../glossary/customer-segment.md)
- [Industry](../glossary/industry.md)
- [Account Tier](../glossary/account-tier.md)
- [Headquarters Country](../glossary/headquarters-country.md)
- [Headquarters Region](../glossary/headquarters-region.md)

---

## Attribute Details

| Attribute | Technical Column | Data Type | Nullable | Key Type | Description |
|-----------|-----------------|-----------|----------|----------|-------------|
| Customer Key | customer_key | integer | No | Primary | Surrogate key uniquely identifying customer |
| Customer ID | customer_id | character varying(20) | No | Business | Business identifier for customer account |
| Customer Name | customer_name | character varying(80) | Yes | - | Official name of customer organization |
| Customer Segment | segment | character varying(30) | Yes | - | Business segment classification |
| Industry | industry | character varying(40) | Yes | - | Industry vertical classification |
| Account Tier | account_tier | character varying(20) | Yes | - | Strategic importance tier |
| Headquarters Country | hq_country | character varying(40) | Yes | - | Country of headquarters location |
| Headquarters Region | hq_region | character varying(20) | Yes | - | Global region of headquarters |

---

## Semantic Links

- [Entity Index](./index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Relationship Index](../relationships/index.md)
- [Measure Index](../measures/index.md)
- [Main Index](../index.md)

---

## Metadata

**Entity ID**: ENT002  
**Domain ID**: DOM001  
**Entity Type**: Dimension  
**Technical Table**: QuoteToBooking.dim_customer  
**Total Attributes**: 8  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
