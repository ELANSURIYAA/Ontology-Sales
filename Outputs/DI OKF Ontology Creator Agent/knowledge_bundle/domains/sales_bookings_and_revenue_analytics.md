---
title: Sales Bookings and Revenue Analytics
type: domain
description: Business domain for completed sales booking analysis across customers, products, partners, geography, contracts, sales representatives, and time.
resource: domains
tags: sales,bookings,revenue,analytics,domain
timestamp: 2026-07-28T00:00:00Z
---

# Sales Bookings and Revenue Analytics

## Business Description

This domain represents sales booking operations for enterprise networking, security, collaboration, observability, and software subscription products. It captures completed customer bookings and supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods.

---

## Business Purpose

The domain provides a consistent analytical structure for measuring booking performance, pricing, discounting, contract value, partner participation, sales coverage, and time-based trends. It serves as the business context for the [Booking Transaction](../entities/booking_transaction.md) fact entity and its related dimensions.

---

## Related Entities

- [Contract](../entities/contract.md)
- [Customer](../entities/customer.md)
- [Date](../entities/date.md)
- [Geography](../entities/geography.md)
- [Partner](../entities/partner.md)
- [Product](../entities/product.md)
- [Sales Representative](../entities/sales_representative.md)
- [Booking Transaction](../entities/booking_transaction.md)

---

## Related Measures

- [Quantity Sold](../measures/quantity_sold.md)
- [Unit List Price USD](../measures/unit_list_price_usd.md)
- [Discount Percentage](../measures/discount_percentage.md)
- [Booking Amount USD](../measures/booking_amount_usd.md)
- [Annual Contract Value USD](../measures/annual_contract_value_usd.md)
- [Total Contract Value USD](../measures/total_contract_value_usd.md)

---

## Related Relationships

- [Contract to Booking Transaction](../relationships/contract_to_booking_transaction.md)
- [Customer to Booking Transaction](../relationships/customer_to_booking_transaction.md)
- [Date to Booking Transaction](../relationships/date_to_booking_transaction.md)
- [Geography to Booking Transaction](../relationships/geography_to_booking_transaction.md)
- [Partner to Booking Transaction](../relationships/partner_to_booking_transaction.md)
- [Product to Booking Transaction](../relationships/product_to_booking_transaction.md)
- [Sales Representative to Booking Transaction](../relationships/sales_representative_to_booking_transaction.md)

---

## Semantic Links

- [Domains Index](index.md)
- [Knowledge Bundle Index](../index.md)
- [Semantic Summary](../semantic_summary.md)
- [Booking Transaction](../entities/booking_transaction.md)
- [Booking Amount USD](../measures/booking_amount_usd.md)
- [Glossary: Booking Transaction](../glossary/booking_transaction.md)
