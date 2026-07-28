---
title: Customer
type: entity
description: Business entity representing customer organizations that place orders and generate bookings
resource: entities
tags: [entity, dimension, customer, account, organization]
timestamp: 2026-07-28T00:00:00Z
---

# Customer

## Business Definition

Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location. The Customer entity enables analysis of booking performance by customer characteristics and supports customer relationship management.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_customer  
**Entity Type**: Dimension  
**Entity ID**: ENT002

---

## Attributes

- **Customer Key** (customer_key) - integer, NOT NULL
- **Customer ID** (customer_id) - character varying(20), NOT NULL
- **Customer Name** (customer_name) - character varying(80), NULL
- **Customer Segment** (segment) - character varying(30), NULL
- **Industry** (industry) - character varying(40), NULL
- **Account Tier** (account_tier) - character varying(20), NULL
- **Headquarters Country** (hq_country) - character varying(40), NULL
- **Headquarters Region** (hq_region) - character varying(20), NULL

---

## Primary Keys

- **Customer Key** (customer_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- [Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md) - Links customers to booking transactions (One-to-Many)

---

## Measures

Customers are analyzed using measures from related booking transactions:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Concepts

### Related Entities
- [Booking Transaction](booking-transaction.md) - Booking transactions placed by this customer
- [Geography](geography.md) - Geographic location of customer transactions
- [Contract](contract.md) - Contracts entered into by customers

### Related Glossary Terms
- [Customer](../glossary/customer.md)
- [Customer Key](../glossary/customer-key.md)
- [Customer ID](../glossary/customer-id.md)
- [Customer Name](../glossary/customer-name.md)
- [Customer Segment](../glossary/customer-segment.md)
- [Industry](../glossary/industry.md)
- [Account Tier](../glossary/account-tier.md)
- [Headquarters Country](../glossary/headquarters-country.md)
- [Headquarters Region](../glossary/headquarters-region.md)

### Related Domains
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Uniqueness**: Each customer record is uniquely identified by Customer Key
2. **Business Identifier**: Customer ID serves as the business identifier for the customer account
3. **Segmentation**: Customer Segment classifies customers into categories such as Enterprise, Service Provider, or Public Sector
4. **Industry Classification**: Industry identifies the business sector in which the customer operates
5. **Account Tiering**: Account Tier indicates the strategic importance or service level of the customer account
6. **Geographic Location**: Headquarters Country and Region identify where the customer organization is based

---

## Usage Examples

### Customer Segmentation Analysis
Analyze booking amounts by customer segment to understand which customer types drive the most revenue.

### Industry Analysis
Evaluate booking performance by industry to identify high-performing sectors and market opportunities.

### Account Tier Analysis
Compare booking amounts and average deal sizes across account tiers to assess strategic account performance.

### Geographic Customer Analysis
Analyze customer distribution and booking performance by headquarters region and country.

### Customer Concentration
Identify top customers by booking amount and assess revenue concentration risk.

---

## Data Quality Notes

- Customer Key is mandatory and serves as the primary key
- Customer ID is mandatory and serves as the business identifier
- Customer Name should be populated for all active customer records
- Segment, Industry, and Account Tier classifications support business analysis
- Headquarters location attributes enable geographic customer analysis
- NULL values in descriptive attributes may indicate incomplete customer profiles

---

## Navigation

- [View Entity Index](index.md)
- [View Related Relationships](../relationships/index.md)
- [View Related Measures](../measures/index.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Entity ID**: ENT002  
**Domain**: Sales Bookings and Revenue Analytics  
**Entity Type**: Dimension  
**Attribute Count**: 8  
**Relationship Count**: 1  
**Last Updated**: 2026-07-28T00:00:00Z
