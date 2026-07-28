---
title: Customer
type: entity
description: Business entity representing the customer account that places orders and generates bookings.
resource: entities
tags: [entity, customer, sales, bookings]
timestamp: 2026-07-28
---

# Customer

## Business Definition
Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location.

## Technical Mapping
- Source Table: `QuoteToBooking.dim_customer`
- Related Glossary: [Customer](../glossary/customer.md)

## Attributes
- Customer Key
- Customer ID
- Customer Name
- Customer Segment
- Industry
- Account Tier
- Headquarters Country
- Headquarters Region

## Primary Keys
- Customer Key

## Foreign Keys
None

## Measures
None

## Relationships
- [Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)

## Related Concepts
- [Customer ID](../glossary/customer-id.md)
- [Customer Name](../glossary/customer-name.md)
- [Customer Segment](../glossary/customer-segment.md)
- [Industry](../glossary/industry.md)
- [Account Tier](../glossary/account-tier.md)
- [Headquarters Country](../glossary/headquarters-country.md)
- [Headquarters Region](../glossary/headquarters-region.md)
- [Booking Transaction](booking-transaction.md)
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

## Business Rules
- Each customer record is uniquely identified by Customer Key.
- Customer ID is the business identifier assigned to the customer account.
- A customer may be associated with multiple booking transactions.
