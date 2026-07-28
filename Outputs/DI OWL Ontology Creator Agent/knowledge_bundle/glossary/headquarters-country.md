---
title: Headquarters Country
type: glossary
description: Country where the customer organization's headquarters is located
resource: glossary
tags: [glossary, customer, country, location, headquarters]
timestamp: 2026-07-28T00:00:00Z
---

# Headquarters Country

## Business Definition

Country where the customer organization's headquarters is located.

---

## Business Meaning

Headquarters Country identifies the nation where the customer's primary corporate headquarters or main office is situated. This geographic attribute enables country-based customer analysis, international market assessment, and regional strategy development. It differs from the transaction geography, which may represent where the sale occurred.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer

**Source Column**: hq_country

**Entity**: [Customer](../entities/customer.md)

**Attribute**: Headquarters Country

**Data Type**: Character Varying(40)

**Confidence Score**: 1.00

---

## Related Concepts

- [Customer](customer.md)
- [Headquarters Region](headquarters-region.md)
- [Geography](geography.md)
- [Country](country.md)

---

## Usage Context

Headquarters Country is used to:
- Identify customer headquarters location
- Enable country-based customer analysis
- Support international market assessment
- Facilitate regional strategy development
- Enable geographic customer distribution analysis

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Customer](../entities/customer.md)
- [Back to Main Index](../index.md)
