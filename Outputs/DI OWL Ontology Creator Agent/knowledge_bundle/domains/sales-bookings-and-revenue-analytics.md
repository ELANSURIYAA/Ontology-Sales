---
title: Sales Bookings and Revenue Analytics
type: domain
description: Business domain for sales booking operations and revenue analysis across enterprise products
resource: domains
tags: [domain, sales, bookings, revenue, analytics, enterprise]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Bookings and Revenue Analytics

## Business Definition

This domain represents sales booking operations for enterprise networking, security, collaboration, observability, and software subscription products. It captures completed customer bookings and supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods.

---

## Business Purpose

The Sales Bookings and Revenue Analytics domain enables comprehensive analysis of:

- **Sales Performance**: Track booking amounts, contract values, and sales volumes across all dimensions
- **Revenue Recognition**: Analyze booking amounts, annual contract values, and total contract values
- **Customer Analytics**: Understand customer segments, industries, and account tiers driving revenue
- **Product Performance**: Evaluate product families, technology domains, and offer types
- **Partner Effectiveness**: Assess partner contributions by type, tier, and route to market
- **Geographic Analysis**: Analyze sales performance by region, theater, and country
- **Sales Team Performance**: Measure sales representative and team effectiveness
- **Contract Management**: Track contract types, terms, renewal behavior, and coverage levels
- **Time-Based Analysis**: Support fiscal and calendar period reporting and trending

---

## Domain Scope

### In Scope
- Completed sales booking transactions
- New sales and renewal bookings
- Enterprise networking products
- Security products
- Collaboration products
- Observability products
- Software subscription products
- SaaS subscription products
- Channel and direct sales
- Customer account management
- Partner ecosystem management
- Contract lifecycle management

### Out of Scope
- Quote management (pre-booking)
- Order fulfillment operations
- Revenue recognition accounting
- Billing and invoicing
- Collections and accounts receivable
- Product delivery and provisioning
- Customer support operations
- Marketing campaigns

---

## Related Entities

### Dimensional Entities

#### [Contract](../entities/contract.md)
Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level.

#### [Customer](../entities/customer.md)
Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location.

#### [Date](../entities/date.md)
Stores calendar and fiscal date attributes used to analyze bookings over time.

#### [Geography](../entities/geography.md)
Stores geographic attributes used to analyze bookings by sales region, theater, and country.

#### [Partner](../entities/partner.md)
Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market.

#### [Product](../entities/product.md)
Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity.

#### [Sales Representative](../entities/sales-representative.md)
Stores information about sales personnel responsible for managing customer relationships and booking transactions.

### Fact Entities

#### [Booking Transaction](../entities/booking-transaction.md)
Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions.

---

## Related Measures

### Volume Metrics
- [Quantity Sold](../measures/quantity-sold.md) - Number of units, licenses, or subscriptions sold

### Pricing Metrics
- [Unit List Price USD](../measures/unit-list-price-usd.md) - Standard list price per unit before discounts
- [Discount Percentage](../measures/discount-percentage.md) - Percentage discount applied to list price

### Revenue Metrics
- [Booking Amount USD](../measures/booking-amount-usd.md) - Total booked revenue after pricing adjustments
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md) - Annualized contract value
- [Total Contract Value USD](../measures/total-contract-value-usd.md) - Total contract value over full term

---

## Related Relationships

### Star Schema Relationships

All dimensional entities connect to the central Booking Transaction fact table:

- [Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)
- [Customer to Booking Transaction](../relationships/customer-to-booking-transaction.md)
- [Date to Booking Transaction](../relationships/date-to-booking-transaction.md)
- [Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)
- [Partner to Booking Transaction](../relationships/partner-to-booking-transaction.md)
- [Product to Booking Transaction](../relationships/product-to-booking-transaction.md)
- [Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)

---

## Key Business Questions

This domain supports analysis of the following business questions:

1. **Revenue Analysis**
   - What is the total booking amount by fiscal quarter and customer segment?
   - What is the annual contract value by product family and geography?
   - What is the total contract value by customer industry and contract type?

2. **Sales Performance**
   - What is the booking amount by sales representative and sales team?
   - What is the average deal size by customer segment and product family?
   - What is the win rate by partner type and sales region?

3. **Product Performance**
   - What is the booking amount by product family and technology domain?
   - What is the quantity sold by offer type and business entity?
   - What is the average unit price by product and customer segment?

4. **Customer Analysis**
   - What is the booking amount by customer segment and industry?
   - What is the average contract value by account tier?
   - What is the customer concentration by headquarters region?

5. **Partner Analysis**
   - What is the booking amount by partner type and partner tier?
   - What is the average discount by route to market?
   - What is the partner contribution by sales region?

6. **Geographic Analysis**
   - What is the booking amount by sales region and theater?
   - What is the growth rate by country and fiscal quarter?
   - What is the market penetration by geography and customer segment?

7. **Contract Analysis**
   - What is the renewal rate by contract type and coverage level?
   - What is the average contract term by customer segment?
   - What is the auto-renew adoption by product family?

---

## Business Rules

### Booking Recognition Rules
- Bookings are recognized when the order is completed and confirmed
- Both new sales and renewals are captured as booking transactions
- Each booking transaction links to exactly one customer, product, partner, geography, sales representative, contract, and date

### Revenue Calculation Rules
- Booking Amount = Quantity × Unit List Price × (1 - Discount Percentage)
- Annual Contract Value = Total Contract Value / Contract Term Months × 12
- Discount Percentage must be between 0 and 100

### Data Quality Rules
- Every booking transaction must have a valid booking date
- Every booking transaction must link to valid dimension records
- Business keys must be unique within each dimension
- Foreign keys must reference existing dimension records

---

## Technical Mapping

**Source Schema**: QuoteToBooking

**Source Tables**:
- dim_contract
- dim_customer
- dim_date
- dim_geography
- dim_partner
- dim_product
- dim_sales_rep
- fact_bookings

**Data Model Pattern**: Star Schema

---

## Semantic Links

### Related Glossary Terms
- [Booking Transaction](../glossary/booking-transaction.md)
- [Booking Amount USD](../glossary/booking-amount-usd.md)
- [Annual Contract Value USD](../glossary/annual-contract-value-usd.md)
- [Total Contract Value USD](../glossary/total-contract-value-usd.md)
- [Customer Segment](../glossary/customer-segment.md)
- [Product Family](../glossary/product-family.md)
- [Partner Type](../glossary/partner-type.md)
- [Sales Region](../glossary/sales-region.md)
- [Contract Type](../glossary/contract-type.md)
- [Fiscal Quarter](../glossary/fiscal-quarter.md)

---

## Navigation

- [View Domain Index](index.md)
- [View All Entities](../entities/index.md)
- [View All Measures](../measures/index.md)
- [View All Relationships](../relationships/index.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Domain ID**: DOM001
**Entity Count**: 8
**Measure Count**: 6
**Relationship Count**: 7
**Last Updated**: 2026-07-28T00:00:00Z
**Format**: Open Knowledge Format (OKF)
