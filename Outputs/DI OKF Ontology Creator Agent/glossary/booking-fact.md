---
title: Booking Fact
type: glossary
description: Stores individual booking transactions and their financial measures for analyzing sales performance
resource: glossary
tags: [okf, glossary, entity, booking, fact]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Fact

## Business Definition

Stores individual booking transactions and their financial measures for analyzing sales performance across customers, products, partners, geographies, contracts, sales representatives, and time.

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings  
**Entity**: Booking Fact  
**Attribute**: N/A (Entity-level term)

---

## Business Meaning

The Booking Fact is the central transactional entity in the Quote to Booking semantic model. It captures every booking transaction at the order line level and includes all measures necessary for comprehensive sales performance analysis. Each record represents a confirmed customer order that has been accepted and recorded in the sales system.

---

## Related Concepts

- [Contract Dimension](contract-dimension.md)
- [Customer Dimension](customer-dimension.md)
- [Date Dimension](date-dimension.md)
- [Geography Dimension](geography-dimension.md)
- [Partner Dimension](partner-dimension.md)
- [Product Dimension](product-dimension.md)
- [Sales Representative Dimension](sales-representative-dimension.md)
- [Booking Amount USD](booking-amount-usd.md)
- [Annual Contract Value USD](annual-contract-value-usd.md)
- [Total Contract Value USD](total-contract-value-usd.md)

---

## Navigation

- [Back to Glossary Index](index.md)
- [Back to Bundle Index](../index.md)
