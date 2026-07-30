---
title: Customer
type: entity
description: Customer organizations that place orders, including identity, segment, industry, account tier, and headquarters location
resource: entities
tags: [customer, accounts, segment, industry, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Customer

## Business Definition

The Customer entity stores descriptive information about customers that place orders, including identity, segment, industry, account tier, and headquarters location. This entity enables customer-centric analysis and segmentation.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_customer  
**Source Schema**: quotetobooking  
**Entity Type**: Dimension  
**Grain**: One row per customer

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

All booking and revenue measures can be analyzed by customer attributes:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

---

## Related Concepts

- [Customer Segment](../glossary/customer-segment.md)
- [Industry](../glossary/industry.md)
- [Account Tier](../glossary/account-tier.md)
- [Headquarters Country](../glossary/hq-country.md)
- [Headquarters Region](../glossary/hq-region.md)

---

## Business Rules

### Customer Identification
Each customer is uniquely identified by customer_key (surrogate key) and customer_id (business key).

### Segment Classification
Customers are classified into market segments such as Enterprise, Service Provider, or Public Sector.

### Account Tier Assignment
Account tier represents the strategic importance or service tier assigned to the customer account.

### Headquarters Location
Headquarters location (country and region) represents the primary location of the customer organization.

---

## Navigation

- [Return to Entities Index](index.md)
- [Return to Main Index](../index.md)
- [View Customers Domain](../domains/customers.md)
