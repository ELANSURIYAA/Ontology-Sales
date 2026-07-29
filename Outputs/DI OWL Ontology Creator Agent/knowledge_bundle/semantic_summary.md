---
title: Semantic Summary
type: index
description: High-level semantic model overview for Sales Bookings and Revenue Analytics
resource: knowledge_bundle
tags: [semantic, summary, overview, model]
timestamp: 2026-07-28T00:00:00Z
---

# Semantic Summary

## Domain Overview

The **Sales Bookings and Revenue Analytics** domain represents sales booking operations for enterprise networking, security, collaboration, observability, and software subscription products. It captures completed customer bookings and supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods.

---

## Semantic Architecture

### Core Fact Entity

**[Booking Transaction](./entities/booking-transaction.md)** - Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions.

### Dimensional Entities

1. **[Contract](./entities/contract.md)** - Commercial agreements associated with bookings
2. **[Customer](./entities/customer.md)** - Organizations that place orders and generate bookings
3. **[Date](./entities/date.md)** - Calendar and fiscal date attributes for temporal analysis
4. **[Geography](./entities/geography.md)** - Geographic attributes for regional analysis
5. **[Partner](./entities/partner.md)** - Channel and direct partners involved in sales
6. **[Product](./entities/product.md)** - Products and offers sold to customers
7. **[Sales Representative](./entities/sales-representative.md)** - Sales personnel managing customer relationships

---

## Key Relationships

All dimensional entities connect to the central **Booking Transaction** fact entity through foreign key relationships:

- [Contract → Booking Transaction](./relationships/contract-to-booking-transaction.md)
- [Customer → Booking Transaction](./relationships/customer-to-booking-transaction.md)
- [Date → Booking Transaction](./relationships/date-to-booking-transaction.md)
- [Geography → Booking Transaction](./relationships/geography-to-booking-transaction.md)
- [Partner → Booking Transaction](./relationships/partner-to-booking-transaction.md)
- [Product → Booking Transaction](./relationships/product-to-booking-transaction.md)
- [Sales Representative → Booking Transaction](./relationships/sales-representative-to-booking-transaction.md)

---

## Key Measures

The model supports six primary financial and operational measures:

1. **[Quantity Sold](./measures/quantity-sold.md)** - Number of units, licenses, or subscriptions
2. **[Unit List Price USD](./measures/unit-list-price-usd.md)** - Standard list price per unit
3. **[Discount Percentage](./measures/discount-percentage.md)** - Percentage discount applied
4. **[Booking Amount USD](./measures/booking-amount-usd.md)** - Total booked revenue amount
5. **[Annual Contract Value USD](./measures/annual-contract-value-usd.md)** - Annualized contract value
6. **[Total Contract Value USD](./measures/total-contract-value-usd.md)** - Total contract value

---

## Business Analysis Capabilities

This semantic model enables analysis across multiple dimensions:

- **Customer Analysis** - Segment, industry, account tier, headquarters location
- **Product Analysis** - Product family, technology domain, offer type, business entity
- **Partner Analysis** - Partner type, partner tier, route to market
- **Geographic Analysis** - Sales region, theater, country
- **Temporal Analysis** - Calendar year, fiscal year, fiscal quarter, fiscal period
- **Sales Performance** - Sales representative, sales role, sales team, covered segment
- **Contract Analysis** - Contract type, term, renewal behavior, coverage level

---

## Technical Foundation

- **Source System:** QuoteToBooking
- **Data Model Pattern:** Star Schema
- **Fact Table:** fact_bookings
- **Dimension Tables:** 7 dimension tables
- **Total Attributes:** 61 attributes
- **Business Keys:** 8 business keys
- **Foreign Keys:** 7 foreign key relationships

---

## Glossary Coverage

The model includes [69 business terms](./glossary/index.md) with complete definitions, technical mappings, and semantic relationships.

---

## Navigation

- [Return to Bundle Index](./index.md)
- [View All Domains](./domains/index.md)
- [View All Entities](./entities/index.md)
- [View All Relationships](./relationships/index.md)
- [View All Measures](./measures/index.md)
- [View Complete Glossary](./glossary/index.md)
