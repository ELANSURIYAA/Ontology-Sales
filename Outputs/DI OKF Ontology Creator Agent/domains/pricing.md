---
title: Pricing Domain
type: domain
description: Pricing attributes used to analyze unit list price and discount characteristics of booked transactions
resource: domains
tags: [okf, domain, pricing, discount, list-price]
timestamp: 2026-07-28T00:00:00Z
---

# Pricing Domain

## Business Definition

The Pricing domain encompasses pricing attributes used to analyze unit list price and discount characteristics of booked transactions. This domain provides the pricing context necessary for pricing strategy analysis and margin management.

---

## Business Purpose

This domain enables business users to:

- Analyze list price trends and variations
- Monitor discount rates and pricing pressure
- Evaluate pricing effectiveness
- Measure price realization
- Support pricing strategy development
- Track margin impact of discounting
- Enable competitive pricing analysis

---

## Domain Scope

### Included
- Unit list prices
- Discount percentages
- Effective pricing calculations
- Price realization metrics

### Excluded
- Cost of goods sold (COGS)
- Margin calculations
- Promotional pricing programs
- Volume-based pricing tiers
- Customer-specific pricing agreements

---

## Related Entities

### Primary Entities
- [Booking Fact](../entities/booking-fact.md)

---

## Related Measures

### Pricing Measures
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)

### Related Measures
- [Quantity Sold](../measures/quantity-sold.md)
- [Booking Amount USD](../measures/booking-amount-usd.md)

---

## Related Relationships

All dimensional relationships to Booking Fact enable pricing analysis by dimension:
- [Customer to Booking](../relationships/customer-to-booking.md)
- [Product to Booking](../relationships/product-to-booking.md)
- [Partner to Booking](../relationships/partner-to-booking.md)
- [Geography to Booking](../relationships/geography-to-booking.md)
- [Sales Representative to Booking](../relationships/sales-representative-to-booking.md)
- [Contract to Booking](../relationships/contract-to-booking.md)
- [Date to Booking](../relationships/date-to-booking.md)

---

## Key Business Concepts

### Unit List Price
Standard list price per unit in U.S. dollars before discounts. This represents the published or catalog price for the product or service.

### Discount Percentage
Discount applied to the list price for the booking line, expressed as a percentage. Discounts may be applied for various reasons including:
- Volume discounts
- Promotional offers
- Competitive pricing
- Strategic account pricing
- Partner program discounts

### Effective Price
The actual price paid after applying discounts:
- **Effective Price = Unit List Price × (1 - Discount Percentage)**

### Price Realization
The percentage of list price actually realized after discounting:
- **Price Realization = (1 - Discount Percentage) × 100%**

---

## Business Rules

1. Unit List Price must be greater than or equal to 0
2. Discount Percentage must be between 0 and 100
3. Effective Price must be non-negative
4. Booking Amount should equal Quantity × Unit List Price × (1 - Discount %)
5. List prices should align with published product pricing
6. Discounts should comply with discount approval policies

---

## Analytical Use Cases

### List Price Analysis
- Track average list prices by product
- Analyze list price trends over time
- Compare list prices across product families
- Monitor list price changes and adjustments

### Discount Analysis
- Monitor average discount rates
- Analyze discount trends over time
- Compare discounts across dimensions (customer, product, partner, geography)
- Identify high-discount transactions requiring review

### Price Realization Analysis
- Calculate price realization rates
- Compare price realization across segments
- Identify pricing pressure by dimension
- Track improvement in price realization

### Pricing Strategy Analysis
- Evaluate pricing effectiveness by segment
- Analyze competitive pricing dynamics
- Support pricing optimization initiatives
- Measure impact of pricing changes

### Margin Impact Analysis
- Assess margin impact of discounting
- Identify margin erosion risks
- Support margin improvement initiatives
- Analyze discount versus volume trade-offs

---

## Data Quality Metrics

### Completeness
- Unit List Price should be populated (>95% target)
- Discount Percentage should be populated (>95% target)
- Pricing measures should be present for all bookings

### Accuracy
- Unit List Price must be non-negative
- Discount Percentage must be between 0 and 100
- Effective prices must reconcile with booking amounts
- List prices should match product catalog

### Consistency
- Pricing should be consistent with product pricing policies
- Discounts should align with approval thresholds
- Pricing calculations should be mathematically correct

---

## Technical Implementation

### Source System
- **Schema**: quotetobooking
- **Table**: fact_bookings
- **Pricing Attributes**: unit_list_price_usd, discount_pct

### Key Attributes
- Unit List Price USD (numeric(12,2))
- Discount Percentage (numeric(5,2))

### Calculated Metrics
- Effective Price = unit_list_price_usd × (1 - discount_pct/100)
- Price Realization = (1 - discount_pct/100) × 100

---

## Semantic Links

### Related Domains
- [Sales Transactions](sales-transactions.md)
- [Revenue Metrics](revenue-metrics.md)
- [Product Management](product-management.md)
- [Customer Management](customer-management.md)
- [Partner Management](partner-management.md)

### Related Glossary Terms
- [Unit List Price USD](../glossary/unit-list-price-usd.md)
- [Discount Percentage](../glossary/discount-percentage.md)
- [Booking Amount USD](../glossary/booking-amount-usd.md)
- [Quantity Sold](../glossary/quantity-sold.md)

---

## Navigation

- [Back to Domains Index](index.md)
- [Back to Bundle Index](../index.md)
