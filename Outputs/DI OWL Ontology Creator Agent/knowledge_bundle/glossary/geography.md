---
title: Geography
type: glossary
description: Stores geographic attributes used to analyze bookings by sales region, theater, and country
resource: glossary
tags: [geography, location, region, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Geography

## Business Definition

Stores geographic attributes used to analyze bookings by sales region, theater, and country.

---

## Business Meaning

The Geography entity provides spatial context for booking transactions, enabling geographic analysis of sales performance across regions, theaters, and countries. It supports territory management and market analysis.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** dim_geography  
**Entity:** [Geography](../entities/geography.md)  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Transactions in geographic locations
- [Geography Key](./geography-key.md) - Unique identifier
- [Sales Region](./sales-region.md) - Regional classification
- [Sales Theater](./sales-theater.md) - Theater classification
- [Country](./country.md) - Country location

---

## Usage Context

Geography is used to:
- Provide spatial context for transactions
- Enable geographic analysis and reporting
- Support territory and market management
- Track regional performance

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/geography.md)
- [Return to Bundle Index](../index.md)
