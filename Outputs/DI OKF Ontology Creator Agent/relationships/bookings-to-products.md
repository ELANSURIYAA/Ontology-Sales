---
title: Bookings to Products
type: relationship
description: Links booking transactions to products
resource: relationships
tags: [bookings, products, many-to-one, relationship]
timestamp: 2026-07-28T00:00:00Z
---

# Bookings to Products

## Business Definition

The Bookings to Products relationship links individual booking transactions to products and service offers. This relationship enables analysis of booking performance by product family, technology domain, offer type, and business entity, supporting product portfolio management and strategic product planning.

---

## Relationship Type

**Many-to-one**

Multiple booking transactions can be associated with the same product.

---

## Source Entity

**[Bookings](../entities/bookings.md)**

The fact table containing individual completed sales booking transactions.

---

## Target Entity

**[Products](../entities/products.md)**

The dimension table containing product and service offer information.

---

## Cardinality

**Many Bookings : One Product**

- Each booking transaction references exactly one product record
- Multiple booking transactions can be associated with the same product
- Product records can exist without associated bookings

---

## Join Specification

### Left Join Key
- **Field**: product_key
- **Entity**: Bookings
- **Type**: Foreign Key

### Right Join Key
- **Field**: product_key
- **Entity**: Products
- **Type**: Primary Key

### Join Condition
```sql
bookings.product_key = products.product_key
```

---

## Technical Mapping

**Source Table**: quotetobooking.fact_bookings

**Target Table**: quotetobooking.dim_product

**Join Column**: product_key

---

## Business Purpose

This relationship enables:

- **Product Family Analysis**: Analyze booking performance by product family
- **Technology Domain Analysis**: Track adoption and performance by technology domain
- **Offer Type Analysis**: Evaluate revenue mix by offer type (hardware, software subscription, SaaS)
- **Business Entity Analysis**: Allocate revenue to business units and portfolios
- **Product Performance**: Rank products by booking contribution
- **Portfolio Management**: Optimize product portfolio and investment decisions

---

## Related Measures

All booking measures can be analyzed by product attributes:
- [Booking Count](../measures/booking-count.md)
- [Total Quantity](../measures/total-quantity.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Average Discount Percentage](../measures/average-discount-pct.md)
- [Average Selling Price USD](../measures/average-selling-price-usd.md)

---

## Related Concepts

- [Product Family](../glossary/product-family.md)
- [Technology Domain](../glossary/technology-domain.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

1. **Mandatory Relationship**: Every booking must reference a valid product
2. **Referential Integrity**: product_key in bookings must exist in products dimension
3. **One Product per Booking**: Each booking references exactly one product record
4. **Product Independence**: Products can exist without bookings (catalog products)

---

## Usage Examples

### Product Family Analysis
```sql
SELECT 
    products.product_family,
    COUNT(bookings.booking_id) as booking_count,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN products ON bookings.product_key = products.product_key
GROUP BY products.product_family
```

### Technology Domain Analysis
```sql
SELECT 
    products.technology_domain,
    SUM(bookings.booking_amount_usd) as total_booking_amount
FROM bookings
JOIN products ON bookings.product_key = products.product_key
GROUP BY products.technology_domain
ORDER BY total_booking_amount DESC
```

---

## Data Quality Rules

- product_key in bookings must not be null
- product_key in bookings must reference valid product_key in products
- No orphaned bookings without product references
- Product dimension must be populated before booking transactions

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
