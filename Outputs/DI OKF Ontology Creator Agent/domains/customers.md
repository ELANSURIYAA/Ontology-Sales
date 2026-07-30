---
title: Customers Domain
type: domain
description: Customer organizations that place orders, including identity, segment, industry, account tier, and headquarters location
resource: domains
tags: [customers, accounts, segment, industry, dimension]
timestamp: 2024-01-15T00:00:00Z
---

# Customers Domain

## Business Definition

The Customers domain stores descriptive information about customers that place orders, including identity, segment, industry, account tier, and headquarters location. This domain enables customer-centric analysis and segmentation.

---

## Business Purpose

The Customers domain enables analysis of:

- Customer segmentation and profiling
- Industry vertical performance
- Account tier and strategic importance
- Geographic distribution of customer base
- Customer-level revenue and booking performance
- Market segment penetration

---

## Domain Type

**Dimension Domain** - Descriptive attributes for customer analysis

---

## Related Entities

- [Customer](../entities/customers.md)

---

## Related Measures

All booking and revenue measures can be analyzed by customer attributes:

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Booking Count](../measures/booking-count.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md)

---

## Related Relationships

- [Bookings to Customers](../relationships/bookings-to-customers.md)

---

## Key Concepts

### Customer Segment
Market segment classification such as Enterprise, Service Provider, or Public Sector.

### Industry
Industry vertical classification for market analysis and targeting.

### Account Tier
Strategic importance or service tier assigned to the customer account.

### Headquarters Location
Geographic location of the customer's headquarters for regional analysis.

---

## Semantic Links

### Related Domains
- [Bookings Domain](bookings.md) - Customer purchases
- [Geographies Domain](geographies.md) - Customer location context
- [Sales Representatives Domain](sales-representatives.md) - Account ownership

### Related Glossary
- [Customer Segment](../glossary/customer-segment.md)
- [Industry](../glossary/industry.md)
- [Account Tier](../glossary/account-tier.md)

---

## Technical Mapping

**Source Table**: quotetobooking.dim_customer  
**Primary Key**: customer_key  
**Business Key**: customer_id

---

## Navigation

- [Return to Domains Index](index.md)
- [Return to Main Index](../index.md)
- [View Customer Entity](../entities/customers.md)
