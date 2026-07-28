---
title: Semantic Summary
type: index
description: Summary of the validated semantic model, extraction results, and OKF bundle coverage.
resource: knowledge_bundle
tags: semantic,summary,validation,okf,sales
timestamp: 2026-07-28T00:00:00Z
---

# Semantic Summary

## Input Validation

- OSI Semantic Model found at `Outputs/DI OSI Semantic Creator Agent/OSI Semantic Model.md`.
- OSI Semantic Model parsed successfully.
- Business Process document found at `Inputs/QuoteToBooking.docx` but the reader returned a UTF-8 decode error.
- Warning retained: process narrative enrichment could not be applied from the business process document.

---

## Semantic Model Validation Results

- Domains present: 1
- Entities present: 8
- Attributes present: 61
- Measures present: 6
- Relationships present: 7
- Glossary terms present: 61
- Duplicate domains detected: None
- Duplicate entities detected: None
- Missing relationships detected: None for declared foreign keys to dimensions
- Missing measures detected: None for declared measure set

---

## Business Domain Extracted

- [Sales Bookings and Revenue Analytics](domains/sales_bookings_and_revenue_analytics.md)

This domain represents sales booking operations for enterprise networking, security, collaboration, observability, and software subscription products. It supports analysis of completed customer bookings across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods.

---

## Entity Coverage

- [Contract](entities/contract.md)
- [Customer](entities/customer.md)
- [Date](entities/date.md)
- [Geography](entities/geography.md)
- [Partner](entities/partner.md)
- [Product](entities/product.md)
- [Sales Representative](entities/sales_representative.md)
- [Booking Transaction](entities/booking_transaction.md)

The semantic model is structured as a star-schema-style analytical design with dimension entities surrounding the transactional fact entity [Booking Transaction](entities/booking_transaction.md).

---

## Relationship Coverage

- [Contract to Booking Transaction](relationships/contract_to_booking_transaction.md)
- [Customer to Booking Transaction](relationships/customer_to_booking_transaction.md)
- [Date to Booking Transaction](relationships/date_to_booking_transaction.md)
- [Geography to Booking Transaction](relationships/geography_to_booking_transaction.md)
- [Partner to Booking Transaction](relationships/partner_to_booking_transaction.md)
- [Product to Booking Transaction](relationships/product_to_booking_transaction.md)
- [Sales Representative to Booking Transaction](relationships/sales_representative_to_booking_transaction.md)

All declared relationships are foreign-key driven one-to-many associations from dimensions into the booking fact.

---

## Measure Coverage

- [Quantity Sold](measures/quantity_sold.md)
- [Unit List Price USD](measures/unit_list_price_usd.md)
- [Discount Percentage](measures/discount_percentage.md)
- [Booking Amount USD](measures/booking_amount_usd.md)
- [Annual Contract Value USD](measures/annual_contract_value_usd.md)
- [Total Contract Value USD](measures/total_contract_value_usd.md)

These measures quantify transaction volume, list pricing, discounting, booked revenue, and contract value.

---

## Business Glossary Coverage

The glossary captures domain concepts, identifiers, descriptive attributes, and transactional metrics. See the full [Glossary Index](glossary/index.md).

---

## Technical Mapping Summary

- Source dimensional tables use the `QuoteToBooking.dim_*` pattern.
- The transactional fact table is `QuoteToBooking.fact_bookings`.
- Surrogate keys are used for dimensions.
- Business identifiers remain available in dimensions for customer, partner, product, and sales representative entities.

---

## Semantic Cross Links

- [Knowledge Bundle Index](index.md)
- [Metrics](metrics.md)
- [Domains Index](domains/index.md)
- [Entities Index](entities/index.md)
- [Relationships Index](relationships/index.md)
- [Measures Index](measures/index.md)
- [Glossary Index](glossary/index.md)
