---
title: Customer
type: entity
description: Customers that place orders and generate bookings including segment, industry, account tier, and headquarters location
resource: entities
tags: [entity, dimension, customer, account, organization]
timestamp: 2026-07-28T00:00:00Z
---

# Customer

## Business Definition

Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer

**Source System**: QuoteToBooking

**Entity Type**: Dimension

---

## Attributes

- **Customer Key** (customer_key): Surrogate key that uniquely identifies a customer record in the customer dimension
- **Customer ID** (customer_id): Business identifier assigned to the customer account
- **Customer Name** (customer_name): Official name of the customer organization that purchased products or services
- **Customer Segment** (segment): Classifies the customer into a business segment such as Enterprise, Service Provider, or Public Sector
- **Industry** (industry): Identifies the industry in which the customer operates
- **Account Tier** (account_tier): Indicates the strategic importance or service tier of the customer account
- **Headquarters Country** (hq_country): Country where the customer organization's headquarters is located
- **Headquarters Region** (hq_region): Global region where the customer organization's headquarters is located

---

## Primary Keys

- **Customer Key** (customer_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- **[Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)**: One-to-Many relationship linking customers to booking transactions

### Related Entities

- [Booking Transaction](booking-transaction.md): Fact entity that references this dimension
- [Geography](geography.md): Related through headquarters location
- [Sales Representative](sales-representative.md): Related through account coverage

---

## Measures

This dimension supports analysis of the following measures:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Concepts

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

## Business Rules

1. Customer Key is a surrogate key and must be unique
2. Customer ID is the business identifier for the customer account
3. Customer Name is the official organization name
4. Customer Segment classifies customers into business categories (Enterprise, Service Provider, Public Sector)
5. Industry identifies the customer's operating industry
6. Account Tier indicates strategic importance or service level
7. Headquarters Country and Region identify the customer's primary location
8. Every booking transaction must reference a valid customer
9. Customer attributes support segmentation and targeting analysis

---

## Usage Examples

**Analysis by Customer Segment**:
- Compare booking amounts across Enterprise, Service Provider, and Public Sector segments
- Analyze product mix by customer segment
- Measure average deal size by segment

**Analysis by Industry**:
- Identify top-performing industries by booking revenue
- Analyze product adoption by industry vertical
- Compare discount rates across industries

**Analysis by Account Tier**:
- Measure revenue contribution by strategic vs. standard accounts
- Analyze contract terms by account tier
- Compare renewal rates across account tiers

**Analysis by Geography**:
- Evaluate booking performance by headquarters region
- Analyze international vs. domestic customer revenue
- Compare customer distribution by country

---

## Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Main Index](../index.md)
- [View Relationships](../relationships/index.md)
- [View Measures](../measures/index.md)
- [View Glossary](../glossary/index.md)
