---
title: Sales Transactions Domain
type: domain
description: Completed customer booking transactions and associated sales performance measures
resource: domains
tags: [okf, domain, sales-transactions, bookings, revenue]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Transactions Domain

## Business Definition

The Sales Transactions domain encompasses completed customer booking transactions and associated sales performance measures across orders, renewals, quantities, pricing, and revenue values. This domain represents the core transactional data that drives sales analytics and revenue reporting.

---

## Business Purpose

This domain serves as the foundation for analyzing sales performance by capturing every booking transaction with complete dimensional context. It enables business users to:

- Track booking revenue across all dimensions
- Analyze sales performance trends over time
- Measure new business versus renewal activity
- Monitor pricing and discount effectiveness
- Calculate contract values and recurring revenue
- Evaluate sales representative and team performance
- Assess product, customer, and partner contribution

---

## Domain Scope

### Included
- Individual booking transactions
- Order and order line details
- Booking types (new business, renewal)
- Quantity and volume measures
- Pricing and discount measures
- Revenue and contract value measures
- Dimensional foreign key relationships

### Excluded
- Quote and opportunity data (pre-booking)
- Invoice and billing data (post-booking)
- Customer master data (covered in Customer Management domain)
- Product master data (covered in Product Management domain)

---

## Related Entities

### Primary Entities
- [Booking Fact](../entities/booking-fact.md)

---

## Related Measures

### Volume Measures
- [Quantity Sold](../measures/quantity-sold.md)

### Pricing Measures
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

### Revenue Measures
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Related Relationships

The Sales Transactions domain connects to all dimensional domains through foreign key relationships:

- [Contract to Booking](../relationships/contract-to-booking.md)
- [Customer to Booking](../relationships/customer-to-booking.md)
- [Date to Booking](../relationships/date-to-booking.md)
- [Geography to Booking](../relationships/geography-to-booking.md)
- [Partner to Booking](../relationships/partner-to-booking.md)
- [Product to Booking](../relationships/product-to-booking.md)
- [Sales Representative to Booking](../relationships/sales-representative-to-booking.md)

---

## Key Business Concepts

### Booking Transaction
A booking transaction represents a confirmed customer order that has been accepted and recorded in the sales system. Each booking includes:
- Unique booking identifier
- Order number and line number
- Transaction date
- Customer, product, and partner references
- Quantity and pricing details
- Revenue and contract values

### Booking Types
- **New Business**: First-time purchase or new product adoption
- **Renewal**: Continuation or extension of existing contract or subscription

### Revenue Recognition
- **Booking Amount**: Total transaction value at time of booking
- **Annual Contract Value (ACV)**: Annualized recurring revenue component
- **Total Contract Value (TCV)**: Full contract value over complete term

---

## Business Rules

1. Every booking transaction must have a unique Booking ID
2. Every booking must reference valid dimensional entities (Customer, Product, Partner, Geography, Sales Rep, Contract, Date)
3. Quantity Sold must be greater than zero
4. Booking Amount must be non-negative
5. Total Contract Value must be greater than or equal to Annual Contract Value
6. Renewal Indicator must align with Booking Type classification
7. Discount Percentage must be between 0 and 100

---

## Analytical Use Cases

### Sales Performance Analysis
- Track total booking revenue by time period
- Analyze booking trends and growth rates
- Compare actual bookings to targets and quotas
- Identify top performing products, customers, and sales representatives

### Revenue Analysis
- Monitor recurring revenue (ACV) versus one-time revenue
- Analyze contract values and deal sizes
- Track revenue by customer segment, industry, and geography
- Measure revenue contribution by product family and technology domain

### Pricing Analysis
- Analyze average selling prices and discount rates
- Identify pricing pressure by segment or product
- Monitor price realization and margin impact
- Compare list prices to effective prices

### Volume Analysis
- Track booking quantities and volume trends
- Analyze product adoption rates
- Measure sales velocity and transaction frequency
- Identify volume drivers by dimension

---

## Data Quality Metrics

### Completeness
- All booking transactions must have complete dimensional references
- All measures must be populated (no null values for critical measures)
- All business keys must be present

### Accuracy
- Revenue calculations must reconcile with source systems
- Dimensional references must be valid
- Booking dates must fall within valid fiscal periods

### Consistency
- Booking Type must align with Renewal Indicator
- Revenue measures must follow logical relationships (TCV ≥ ACV)
- Quantities and prices must produce correct booking amounts

---

## Technical Implementation

### Source System
- **Schema**: quotetobooking
- **Table**: fact_bookings
- **Grain**: Individual booking transaction line
- **Load Frequency**: Daily

### Key Attributes
- Booking ID (Primary Key)
- Order Number, Order Line Number (Business Keys)
- 7 Foreign Keys (Customer, Product, Partner, Geography, Sales Rep, Contract, Date)
- 6 Measures (Quantity, Unit Price, Discount %, Booking Amount, ACV, TCV)
- 2 Classification Attributes (Booking Type, Renewal Indicator)

---

## Semantic Links

### Related Domains
- [Customer Management](customer-management.md)
- [Product Management](product-management.md)
- [Partner Management](partner-management.md)
- [Geography](geography.md)
- [Sales Organization](sales-organization.md)
- [Contract Management](contract-management.md)
- [Time Management](time-management.md)
- [Pricing](pricing.md)
- [Revenue Metrics](revenue-metrics.md)

### Related Glossary Terms
- [Booking Fact](../glossary/booking-fact.md)
- [Booking Amount USD](../glossary/booking-amount-usd.md)
- [Annual Contract Value USD](../glossary/annual-contract-value-usd.md)
- [Total Contract Value USD](../glossary/total-contract-value-usd.md)
- [Booking Type](../glossary/booking-type.md)
- [Renewal Indicator](../glossary/renewal-indicator.md)

---

## Navigation

- [Back to Domains Index](index.md)
- [Back to Bundle Index](../index.md)
