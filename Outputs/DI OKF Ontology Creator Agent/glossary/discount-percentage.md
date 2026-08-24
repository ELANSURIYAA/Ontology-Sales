---
title: Discount Percentage
type: glossary
description: The discount applied to products or services as a percentage of list price
resource: glossary
tags: [discount, pricing, percentage]
timestamp: 2026-07-28T00:00:00Z
---

# Discount Percentage

## Business Definition

Discount Percentage is the discount applied to products or services, expressed as a fractional percentage of the list price. It represents the price reduction offered to customers as part of the sales negotiation and pricing strategy.

---

## Business Meaning

Discount Percentage is a key pricing metric that reflects:
- Pricing flexibility and negotiation outcomes
- Competitive positioning and market dynamics
- Customer value perception
- Sales strategy effectiveness
- Margin impact on profitability

Discounts are used to:
- Win competitive deals
- Incentivize larger purchases
- Reward strategic customers
- Clear inventory or capacity
- Respond to market conditions
- Support channel partners

---

## Technical Mapping

**Source Entity**: [Bookings](../entities/bookings.md)

**Source Field**: discount_pct

**Format**: Fractional decimal (0.00 to 1.00)

---

## Synonyms

- Discount Rate
- Price Discount
- Discount Factor
- Price Reduction
- Markdown

---

## Related Concepts

- [Booking Amount](./booking-amount.md) - Net amount after discount
- [Booking Transaction](./booking-transaction.md) - Transaction containing discount

---

## Related Entities

- [Bookings](../entities/bookings.md) - Contains discount percentage values

---

## Related Measures

- [Average Discount Percentage](../measures/average-discount-pct.md) - Average discount across bookings
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md) - Revenue after discounts
- [Average Selling Price USD](../measures/average-selling-price-usd.md) - Price after discounts

---

## Usage Context

Discount Percentage is used for:
- Pricing strategy analysis
- Margin management
- Competitive analysis
- Sales behavior monitoring
- Channel pricing evaluation
- Deal approval workflows
- Profitability analysis

---

## Business Rules

1. Discount percentage is stored as a fractional decimal (0.00 to 1.00)
2. 0.00 represents no discount (0%)
3. 0.15 represents a 15% discount
4. 1.00 represents a 100% discount (free)
5. Discount percentage must be between 0 and 1
6. Booking amount = quantity × unit_list_price × (1 - discount_pct)

---

## Calculation Example

**Example 1: 15% Discount**
- Unit List Price: $1,000
- Discount Percentage: 0.15 (15%)
- Discount Amount: $1,000 × 0.15 = $150
- Net Price: $1,000 × (1 - 0.15) = $850

**Example 2: No Discount**
- Unit List Price: $1,000
- Discount Percentage: 0.00 (0%)
- Discount Amount: $0
- Net Price: $1,000

**Example 3: 25% Discount**
- Unit List Price: $1,000
- Discount Percentage: 0.25 (25%)
- Discount Amount: $1,000 × 0.25 = $250
- Net Price: $1,000 × (1 - 0.25) = $750

---

## Display Format

For reporting and display purposes, discount percentage is typically:
- Multiplied by 100 to convert to percentage format
- Displayed with percentage symbol (%)
- Example: 0.15 displayed as "15%"

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
