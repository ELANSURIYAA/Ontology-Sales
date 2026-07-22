---
title: Semantic Summary
type: semantic_summary
domain: Sales Bookings and Revenue Analytics
version: 1.0
status: generated
---

# Semantic Summary

## Overview

The semantic model describes a star-schema-oriented analytics domain for completed sales bookings. The central business event is the [Booking Transaction](entities/booking-transaction.md), which is analyzed across customer, product, partner, geography, sales representative, contract, and date perspectives.

## Business Domain

- [Sales Bookings and Revenue Analytics](domains/sales-bookings-and-revenue-analytics.md)

## Business Entities

- [Contract](entities/contract.md)
- [Customer](entities/customer.md)
- [Date](entities/date.md)
- [Geography](entities/geography.md)
- [Partner](entities/partner.md)
- [Product](entities/product.md)
- [Sales Representative](entities/sales-representative.md)
- [Booking Transaction](entities/booking-transaction.md)

## Relationships

All declared semantic relationships are referential one-to-many relationships from analytic dimensions to the booking transaction fact entity:

- [Contract to Booking Transaction](relationships/contract-to-booking-transaction.md)
- [Customer to Booking Transaction](relationships/customer-to-booking-transaction.md)
- [Date to Booking Transaction](relationships/date-to-booking-transaction.md)
- [Geography to Booking Transaction](relationships/geography-to-booking-transaction.md)
- [Partner to Booking Transaction](relationships/partner-to-booking-transaction.md)
- [Product to Booking Transaction](relationships/product-to-booking-transaction.md)
- [Sales Representative to Booking Transaction](relationships/sales-representative-to-booking-transaction.md)

## Measures

Measures are primarily associated with the [Booking Transaction](entities/booking-transaction.md) entity:

- [Quantity Sold](measures/quantity-sold.md)
- [Unit List Price USD](measures/unit-list-price-usd.md)
- [Discount Percentage](measures/discount-percentage.md)
- [Booking Amount USD](measures/booking-amount-usd.md)
- [Annual Contract Value USD](measures/annual-contract-value-usd.md)
- [Total Contract Value USD](measures/total-contract-value-usd.md)

## Validation Warnings

- The business process source document could not be parsed by the provided reader due to encoding/readability constraints.
- Business context enrichment therefore relies on the validated OSI Semantic Model only.
- The glossary mapping includes many attribute-level terms; this bundle generates core concept glossary documents for major reusable business concepts to avoid duplication with entity and measure pages.