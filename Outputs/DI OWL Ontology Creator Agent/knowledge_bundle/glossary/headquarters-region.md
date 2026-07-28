---
title: Headquarters Region
type: glossary
description: Global region where the customer organization's headquarters is located
resource: glossary
tags: [glossary, customer, region, location, headquarters]
timestamp: 2026-07-28T00:00:00Z
---

# Headquarters Region

## Business Definition

Global region where the customer organization's headquarters is located.

---

## Business Meaning

Headquarters Region identifies the broader geographic region where the customer's primary corporate headquarters is situated. Regions typically represent major global markets such as Americas, EMEA (Europe, Middle East, Africa), Asia Pacific, or other strategic geographic groupings. This enables high-level geographic customer analysis and regional market strategy.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_customer

**Source Column**: hq_region

**Entity**: [Customer](../entities/customer.md)

**Attribute**: Headquarters Region

**Data Type**: Character Varying(20)

**Confidence Score**: 1.00

---

## Related Concepts

- [Customer](customer.md)
- [Headquarters Country](headquarters-country.md)
- [Geography](geography.md)
- [Sales Region](sales-region.md)

---

## Usage Context

Headquarters Region is used to:
- Identify customer headquarters region
- Enable regional customer analysis
- Support global market assessment
- Facilitate regional strategy development
- Enable geographic customer distribution analysis

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Customer](../entities/customer.md)
- [Back to Main Index](../index.md)
