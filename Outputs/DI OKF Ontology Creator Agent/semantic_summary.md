---
title: Semantic Summary
type: index
description: Complete semantic model architecture overview including domains, entities, relationships, and measures
resource: knowledge_bundle
tags: [semantic-model, architecture, overview, sales, bookings]
timestamp: 2026-07-28T00:00:00Z
---

# Semantic Summary

## Model Overview

**Model Name**: Sales Bookings and Revenue Analytics

**Version**: 0.1

**Description**: Sales bookings and revenue analytics semantic model for completed booking transactions across customers, products, partners, geographies, sales representatives, contracts, and reporting periods.

---

## AI Context

Use this semantic model for sales booking and revenue analysis. Booking transactions are represented at the booking transaction grain in the bookings dataset. Use booking date for time-based analysis and the defined metrics for booking amount, ACV, TCV, quantity, discount, renewal, and order analysis.

---

## Business Domains

### [Sales Bookings and Revenue Analytics](./domains/sales-bookings-and-revenue-analytics.md)
Primary business domain covering all sales booking transactions, revenue metrics, and dimensional analysis across customers, products, partners, geographies, sales representatives, contracts, and time periods.

---

## Business Entities

The semantic model contains **8 core business entities**:

1. **[Bookings](./entities/bookings.md)** - Fact table capturing individual completed sales booking transactions
2. **[Customers](./entities/customers.md)** - Customer dimension with segment, industry, and location attributes
3. **[Products](./entities/products.md)** - Product dimension with family, technology domain, and offer type
4. **[Partners](./entities/partners.md)** - Partner dimension with type, tier, and route to market
5. **[Geographies](./entities/geographies.md)** - Geographic dimension with region, theater, and country
6. **[Sales Representatives](./entities/sales-representatives.md)** - Sales rep dimension with role, team, and segment coverage
7. **[Contracts](./entities/contracts.md)** - Contract dimension with type, term, and coverage level
8. **[Dates](./entities/dates.md)** - Time dimension with calendar and fiscal attributes

---

## Relationships

The model defines **7 core relationships** connecting bookings to dimensional entities:

1. **[Bookings to Contracts](./relationships/bookings-to-contracts.md)** - Many-to-one relationship linking bookings to contract terms
2. **[Bookings to Customers](./relationships/bookings-to-customers.md)** - Many-to-one relationship linking bookings to customers
3. **[Bookings to Dates](./relationships/bookings-to-dates.md)** - Many-to-one relationship linking bookings to time periods
4. **[Bookings to Geographies](./relationships/bookings-to-geographies.md)** - Many-to-one relationship linking bookings to geographic territories
5. **[Bookings to Partners](./relationships/bookings-to-partners.md)** - Many-to-one relationship linking bookings to sales partners
6. **[Bookings to Products](./relationships/bookings-to-products.md)** - Many-to-one relationship linking bookings to products
7. **[Bookings to Sales Representatives](./relationships/bookings-to-sales-representatives.md)** - Many-to-one relationship linking bookings to sales reps

---

## Business Measures

The model provides **11 key business measures**:

### Volume Metrics
- **[Booking Count](./measures/booking-count.md)** - Count of booking transaction records
- **[Distinct Order Count](./measures/distinct-order-count.md)** - Count of distinct sales orders
- **[Total Quantity](./measures/total-quantity.md)** - Total units, licenses, or services booked

### Revenue Metrics
- **[Total Booking Amount USD](./measures/total-booking-amount-usd.md)** - Total booked sales amount
- **[Total ACV USD](./measures/total-acv-usd.md)** - Total annual contract value
- **[Total TCV USD](./measures/total-tcv-usd.md)** - Total contract value

### Pricing Metrics
- **[Average Discount Percentage](./measures/average-discount-pct.md)** - Average discount applied
- **[Average Selling Price USD](./measures/average-selling-price-usd.md)** - Average revenue per unit
- **[Average Booking Value USD](./measures/average-booking-value-usd.md)** - Average booking value per transaction

### Renewal Metrics
- **[Renewal Booking Amount USD](./measures/renewal-booking-amount-usd.md)** - Total renewal booking amount
- **[Net New Booking Amount USD](./measures/net-new-booking-amount-usd.md)** - Total net new booking amount

---

## Data Architecture

### Grain
The model operates at the **booking transaction grain**, with each record in the bookings fact table representing a single completed booking transaction.

### Source System
**Source**: quotetobooking schema

### Key Datasets
- **Fact Table**: quotetobooking.fact_bookings
- **Dimension Tables**: 
  - quotetobooking.dim_customer
  - quotetobooking.dim_product
  - quotetobooking.dim_partner
  - quotetobooking.dim_geography
  - quotetobooking.dim_sales_rep
  - quotetobooking.dim_contract
  - quotetobooking.dim_date

---

## Semantic Cross-References

### Related Glossary Terms
- [Booking Transaction](./glossary/booking-transaction.md)
- [Annual Contract Value](./glossary/annual-contract-value.md)
- [Total Contract Value](./glossary/total-contract-value.md)
- [Renewal](./glossary/renewal.md)
- [Net New Business](./glossary/net-new-business.md)
- [Customer Segment](./glossary/customer-segment.md)
- [Product Family](./glossary/product-family.md)
- [Technology Domain](./glossary/technology-domain.md)
- [Partner Type](./glossary/partner-type.md)
- [Route to Market](./glossary/route-to-market.md)
- [Fiscal Period](./glossary/fiscal-period.md)

---

## Model Validation

✓ All entities have primary keys defined  
✓ All relationships have valid join keys  
✓ All measures have valid expressions  
✓ All foreign keys reference valid dimensions  
✓ No duplicate entities detected  
✓ No duplicate relationships detected  
✓ No orphaned measures detected  

---

## Usage Guidance

This semantic model should be used for:
- Sales booking performance analysis
- Revenue trend analysis by time period
- Customer segment and industry analysis
- Product family and technology domain analysis
- Partner and channel performance analysis
- Geographic territory analysis
- Sales representative performance analysis
- Contract type and renewal analysis
- Discount and pricing analysis
- ACV and TCV tracking
