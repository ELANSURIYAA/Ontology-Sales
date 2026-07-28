---
title: Semantic Summary
type: index
description: Summary of the semantic scope, structure, and validation results for the sales bookings and revenue analytics knowledge bundle.
resource: knowledge_bundle
tags: [summary, semantic-model, sales, bookings, okf]
timestamp: 2026-07-28
---

# Semantic Summary

## Business Scope
The semantic model represents sales booking operations for enterprise networking, security, collaboration, observability, and software subscription products. It captures completed customer bookings and supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods.

## Semantic Structure
- Domain: [Sales Bookings and Revenue Analytics](domains/sales-bookings-and-revenue-analytics.md)
- Fact-style entity: [Booking Transaction](entities/booking-transaction.md)
- Dimensions: [Contract](entities/contract.md), [Customer](entities/customer.md), [Date](entities/date.md), [Geography](entities/geography.md), [Partner](entities/partner.md), [Product](entities/product.md), [Sales Representative](entities/sales-representative.md)
- Measures: [Quantity Sold](measures/quantity-sold.md), [Unit List Price USD](measures/unit-list-price-usd.md), [Discount Percentage](measures/discount-percentage.md), [Booking Amount USD](measures/booking-amount-usd.md), [Annual Contract Value USD](measures/annual-contract-value-usd.md), [Total Contract Value USD](measures/total-contract-value-usd.md)

## Relationship Pattern
The model follows a star-schema-oriented analytical pattern in which Booking Transaction references conformed dimensions through foreign keys.

- [Contract to Booking Transaction](relationships/contract-to-booking-transaction.md)
- [Customer to Booking Transaction](relationships/customer-to-booking-transaction.md)
- [Date to Booking Transaction](relationships/date-to-booking-transaction.md)
- [Geography to Booking Transaction](relationships/geography-to-booking-transaction.md)
- [Partner to Booking Transaction](relationships/partner-to-booking-transaction.md)
- [Product to Booking Transaction](relationships/product-to-booking-transaction.md)
- [Sales Representative to Booking Transaction](relationships/sales-representative-to-booking-transaction.md)

## Validation Findings
- Semantic model structure parsed successfully.
- Required sections found: Domains, Entities, Attributes, Measures, Relationships, Glossary Mapping.
- Duplicate domains detected: none.
- Duplicate entities detected: none.
- Missing relationships detected: none for declared foreign keys.
- Missing measures detected: none for declared measure section.
- Warning: the business process document at `Inputs/QuoteToBooking.docx` was not readable through the provided tool because the file could not be decoded as UTF-8.

## Technical Mapping Coverage
All entities and glossary concepts include technical mappings to the `QuoteToBooking` schema objects:
- `QuoteToBooking.dim_contract`
- `QuoteToBooking.dim_customer`
- `QuoteToBooking.dim_date`
- `QuoteToBooking.dim_geography`
- `QuoteToBooking.dim_partner`
- `QuoteToBooking.dim_product`
- `QuoteToBooking.dim_sales_rep`
- `QuoteToBooking.fact_bookings`

## Navigation
- [Knowledge Bundle Index](index.md)
- [Metrics](metrics.md)
- [Domains Index](domains/index.md)
- [Entities Index](entities/index.md)
- [Relationships Index](relationships/index.md)
- [Measures Index](measures/index.md)
- [Glossary Index](glossary/index.md)
