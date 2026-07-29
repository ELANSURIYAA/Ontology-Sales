---
title: Customer Dimension
type: entity
description: Customer master data used to analyze bookings by customer identity, segment, and industry
resource: entities
tags: [okf, entity, customer, dimension, customer-management]
timestamp: 2026-07-28T00:00:00Z
---

# Customer Dimension

## Business Definition

The Customer Dimension stores descriptive customer attributes used to analyze bookings by customer identity, segment, industry, account tier, and headquarters location. This dimension enables customer-centric sales analytics and supports customer segmentation and account management.

---

## Technical Mapping

**Source Schema**: quotetobooking  
**Source Table**: dim_customer  
**Entity Type**: Dimension  
**Grain**: One record per unique customer

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

None (this is a dimension table)

---

## Relationships

### Outbound Relationships
- [Customer to Booking](../relationships/customer-to-booking.md) - One-to-Many relationship to Booking Fact

---

## Measures

All booking measures can be analyzed by customer attributes:

- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Related Concepts

### Related Entities
- [Booking Fact](booking-fact.md)
- [Geography Dimension](geography-dimension.md)

### Related Domains
- [Customer Management](../domains/customer-management.md)
- [Sales Transactions](../domains/sales-transactions.md)
- [Geography](../domains/geography.md)

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

## Business Rules

1. Customer Key must be unique and not null
2. Customer ID must be unique and not null
3. Customer Name is required for all records
4. Customer Segment should be populated for all customers
5. Headquarters Country and Region should align with standard geographic hierarchies
6. Account Tier should reflect current strategic classification

---

## Attribute Details

### customer_key
- **Data Type**: integer
- **Nullable**: No
- **Primary Key**: Yes
- **Description**: Surrogate key that uniquely identifies a customer record in the customer dimension

### customer_id
- **Data Type**: character varying(20)
- **Nullable**: No
- **Description**: Business identifier assigned to the customer account

### customer_name
- **Data Type**: character varying(80)
- **Nullable**: Yes
- **Description**: Name of the customer organization that placed the order

### segment
- **Data Type**: character varying(30)
- **Nullable**: Yes
- **Description**: Market segment to which the customer belongs, such as Enterprise, Service Provider, or Public Sector

### industry
- **Data Type**: character varying(40)
- **Nullable**: Yes
- **Description**: Industry classification of the customer organization

### account_tier
- **Data Type**: character varying(20)
- **Nullable**: Yes
- **Description**: Strategic importance or tier assigned to the customer account

### hq_country
- **Data Type**: character varying(40)
- **Nullable**: Yes
- **Description**: Country where the customer organization's headquarters is located

### hq_region
- **Data Type**: character varying(20)
- **Nullable**: Yes
- **Description**: Global region where the customer headquarters is located

---

## Analytical Use Cases

- Analyze bookings by customer segment
- Track revenue by industry vertical
- Evaluate account tier profitability
- Monitor geographic customer distribution
- Identify strategic customer relationships
- Support customer segmentation analysis

---

## Data Quality Metrics

- **Completeness**: Customer Key and Customer ID must be 100% populated
- **Uniqueness**: Customer Key and Customer ID must be unique
- **Validity**: Segment and Account Tier must match approved values
- **Consistency**: Headquarters Region must align with Headquarters Country

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Bundle Index](../index.md)
