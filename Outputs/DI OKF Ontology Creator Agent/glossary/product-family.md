---
title: Product Family
type: glossary
description: Higher-level grouping of related products within the portfolio
resource: glossary
tags: [product-family, product, portfolio]
timestamp: 2026-07-28T00:00:00Z
---

# Product Family

## Business Definition

Product Family is a higher-level grouping of related products within the product portfolio. Product families organize individual products into logical categories based on shared characteristics, functionality, or market positioning.

---

## Business Meaning

Product Family is used to:
- Organize products into manageable categories
- Support portfolio management and planning
- Enable family-level performance analysis
- Guide product development and investment decisions
- Simplify product positioning and messaging
- Support cross-sell and upsell strategies

Product families typically group products that:
- Share common technology or architecture
- Target similar use cases or customer needs
- Belong to the same solution area
- Have related functionality or features
- Are positioned together in the market

---

## Technical Mapping

**Source Entity**: [Products](../entities/products.md)

**Source Field**: product_family

---

## Synonyms

- Product Line
- Product Group
- Product Category
- Product Portfolio
- Solution Family

---

## Related Concepts

- [Technology Domain](./technology-domain.md) - Technology area for the product
- [Booking Transaction](./booking-transaction.md) - Transactions analyzed by product family

---

## Related Entities

- [Products](../entities/products.md) - Contains product family classification

---

## Related Measures

All booking measures can be analyzed by product family:
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total Quantity](../measures/total-quantity.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)

---

## Usage Context

Product Family is used for:
- Product portfolio analysis
- Revenue reporting by product line
- Product performance tracking
- Investment prioritization
- Product roadmap planning
- Cross-sell and upsell identification
- Competitive positioning

---

## Business Rules

1. Each product belongs to exactly one product family
2. Product families are defined at a higher level than individual SKUs
3. Product family classification is consistent across the organization
4. Product families may contain multiple individual products

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
