---
title: Customer
type: glossary
description: Customer organizations that place orders and generate bookings including segment, industry, account tier, and headquarters location
resource: glossary
tags: [glossary, customer, organization, account]
timestamp: 2026-07-28T00:00:00Z
---

# Customer

## Business Definition

Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location.

---

## Business Meaning

A customer represents an organization that purchases products and services from the company. Customers are the primary source of revenue and are characterized by various attributes including business segment, industry vertical, strategic importance, and geographic location. Understanding customer characteristics is essential for sales strategy, market segmentation, and revenue analysis.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_customer  
**Entity**: [Customer](../entities/customer.md)  
**Confidence Score**: 1.00

---

## Synonyms

- Account
- Client
- Customer Organization
- Customer Account

---

## Related Concepts

### Related Entities
- [Customer](../entities/customer.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Attributes
- [Customer Key](customer-key.md)
- [Customer ID](customer-id.md)
- [Customer Name](customer-name.md)
- [Customer Segment](customer-segment.md)
- [Industry](industry.md)
- [Account Tier](account-tier.md)
- [Headquarters Country](headquarters-country.md)
- [Headquarters Region](headquarters-region.md)

### Related Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)

---

## Usage Context

Customers are used to:
- Track revenue by customer organization
- Segment markets and analyze performance
- Manage customer relationships
- Identify strategic accounts
- Analyze customer lifetime value

---

## Examples

- Enterprise customer in financial services
- Service provider in telecommunications
- Public sector customer in government
- Mid-market customer in healthcare

---

## Navigation

- [View Glossary Index](index.md)
- [View Customer Entity](../entities/customer.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Entity  
**Source Entity**: Customer  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
