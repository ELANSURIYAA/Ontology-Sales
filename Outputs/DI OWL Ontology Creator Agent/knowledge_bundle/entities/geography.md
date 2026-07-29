---
title: Geography
type: entity
description: Geographic attributes used to analyze bookings by sales region, theater, and country
resource: entities
tags: [geography, location, region, theater, dimension]
timestamp: 2026-07-28T00:00:00Z
---

# Geography

## Business Definition

Stores geographic attributes used to analyze bookings by sales region, theater, and country. The Geography entity enables spatial analysis of sales performance across different geographic markets and territories.

---

## Entity Identifier

**Entity ID:** ENT004  
**Domain:** [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_geography  
**Table Type:** Dimension Table

---

## Attributes

- **Geography Key** - Surrogate key that uniquely identifies a geography record in the geography dimension
- **Sales Region** - High-level geographic region used for reporting and performance analysis
- **Sales Theater** - Subregional sales area or theater used to organize market coverage and reporting
- **Country** - Country associated with the geography record

---

## Primary Keys

- **Geography Key** (geography_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- **[Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)** - One-to-Many relationship linking geographies to booking transactions

---

## Measures

Geographies enable regional analysis of all measures from [Booking Transaction](./booking-transaction.md) entity:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)

---

## Business Rules

1. Each geography must have a unique Geography Key
2. Sales Region represents the highest level of geographic hierarchy
3. Sales Theater provides subregional market segmentation
4. Country enables country-level performance analysis
5. Geographic hierarchy supports drill-down analysis from region to theater to country

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Transactions occurring in specific geographies
- [Customer](./customer.md) - Customers located in different geographies
- [Sales Representative](./sales-representative.md) - Sales representatives covering geographic territories
- [Partner](./partner.md) - Partners operating in specific geographies

---

## Glossary Terms

- [Geography](../glossary/geography.md)
- [Geography Key](../glossary/geography-key.md)
- [Sales Region](../glossary/sales-region.md)
- [Sales Theater](../glossary/sales-theater.md)
- [Country](../glossary/country.md)

---

## Navigation

- [Return to Entities Index](./index.md)
- [Return to Bundle Index](../index.md)
- [View Domain](../domains/sales-bookings-and-revenue-analytics.md)
- [View Relationships](../relationships/index.md)
