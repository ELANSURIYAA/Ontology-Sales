---
title: Sales Representative ID
type: glossary
description: Business identifier assigned to the sales representative
resource: glossary
tags: [glossary, sales-representative, identifier, business-key]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative ID

## Business Definition

Business identifier assigned to the sales representative.

---

## Business Meaning

Sales Representative ID is the business-recognized identifier used to uniquely identify sales personnel in operational systems, HR systems, and business processes. Unlike the surrogate Sales Representative Key, the Sales Representative ID is meaningful to business users and is used in sales reporting, quota management, and commission calculations.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_sales_rep

**Source Column**: rep_id

**Entity**: [Sales Representative](../entities/sales-representative.md)

**Attribute**: Sales Representative ID

**Data Type**: Character Varying(20)

**Confidence Score**: 1.00

---

## Related Concepts

- [Sales Representative](sales-representative.md)
- [Sales Representative Key](sales-representative-key.md)
- [Sales Representative Name](sales-representative-name.md)

---

## Usage Context

Sales Representative ID is used to:
- Identify sales personnel in business processes
- Support sales representative lookup and reference
- Enable cross-system sales representative identification
- Facilitate quota and commission management
- Support sales operations

---

## Navigation

- [Back to Glossary Index](index.md)
- [View Entity: Sales Representative](../entities/sales-representative.md)
- [Back to Main Index](../index.md)
