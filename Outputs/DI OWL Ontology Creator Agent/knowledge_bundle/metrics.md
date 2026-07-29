---
title: Business Metrics Catalog
type: index
description: Comprehensive catalog of business measures and KPIs for sales booking and revenue analytics
resource: knowledge_bundle
tags: [metrics, measures, kpi, financial, revenue, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Business Metrics Catalog

## Overview

This catalog documents all business measures and key performance indicators (KPIs) used in the Sales Bookings and Revenue Analytics domain. These metrics enable comprehensive financial analysis, performance tracking, and strategic decision-making.

---

## Measure Categories

### Volume Metrics

Measures tracking transaction volumes and quantities:

- **[Quantity Sold](./measures/quantity-sold.md)** - Units, licenses, or subscriptions sold

### Pricing Metrics

Measures related to product pricing and discounting:

- **[Unit List Price USD](./measures/unit-list-price-usd.md)** - Standard list price per unit
- **[Discount Percentage](./measures/discount-percentage.md)** - Price discount percentage

### Revenue Metrics

Measures tracking booked revenue and financial performance:

- **[Booking Amount USD](./measures/booking-amount-usd.md)** - Total booked revenue
- **[Annual Contract Value USD](./measures/annual-contract-value-usd.md)** - Annualized contract value (ACV)
- **[Total Contract Value USD](./measures/total-contract-value-usd.md)** - Total contract value (TCV)

---

## Detailed Measure Specifications

### Quantity Sold

**Business Definition**: Number of units, licenses, or subscriptions included in the booking transaction  
**Technical Column**: `quantity`  
**Aggregation**: SUM  
**Data Type**: Integer  
**Source Entity**: [Booking Transaction](./entities/booking-transaction.md)

**Usage**:
- Volume analysis
- Product adoption tracking
- Sales performance measurement
- Capacity planning

---

### Unit List Price USD

**Business Definition**: Standard list price per unit in U.S. dollars before discounts are applied  
**Technical Column**: `unit_list_price_usd`  
**Aggregation**: SUM  
**Data Type**: Numeric  
**Source Entity**: [Booking Transaction](./entities/booking-transaction.md)

**Usage**:
- Pricing strategy analysis
- List price management
- Price positioning
- Revenue potential calculation

---

### Discount Percentage

**Business Definition**: Percentage discount applied to the list price for the booking transaction  
**Technical Column**: `discount_pct`  
**Aggregation**: AVG  
**Data Type**: Numeric  
**Source Entity**: [Booking Transaction](./entities/booking-transaction.md)

**Usage**:
- Discount analysis
- Pricing effectiveness
- Margin management
- Competitive positioning

---

### Booking Amount USD

**Business Definition**: Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments  
**Technical Column**: `booking_amount_usd`  
**Aggregation**: SUM  
**Data Type**: Numeric  
**Source Entity**: [Booking Transaction](./entities/booking-transaction.md)

**Usage**:
- Revenue reporting
- Sales performance tracking
- Quota attainment
- Financial forecasting

**Formula**: `Quantity × Unit List Price × (1 - Discount Percentage)`

---

### Annual Contract Value USD

**Business Definition**: Annualized value of the contract associated with the booking in U.S. dollars  
**Technical Column**: `acv_usd`  
**Aggregation**: SUM  
**Data Type**: Numeric  
**Source Entity**: [Booking Transaction](./entities/booking-transaction.md)

**Usage**:
- Subscription revenue analysis
- Recurring revenue tracking
- Customer lifetime value
- Growth rate calculation

**Formula**: `Total Contract Value ÷ Contract Term (Years)`

---

### Total Contract Value USD

**Business Definition**: Total value of the full contract associated with the booking in U.S. dollars  
**Technical Column**: `tcv_usd`  
**Aggregation**: SUM  
**Data Type**: Numeric  
**Source Entity**: [Booking Transaction](./entities/booking-transaction.md)

**Usage**:
- Contract value analysis
- Long-term revenue planning
- Deal size tracking
- Pipeline management

**Formula**: `Booking Amount × Contract Term (Months) ÷ 12`

---

## Analytical Dimensions

All measures can be analyzed across the following business dimensions:

### Temporal Analysis
- **[Date](./entities/date.md)** - Calendar year, fiscal year, quarter, month, period

### Geographic Analysis
- **[Geography](./entities/geography.md)** - Region, theater, country

### Customer Analysis
- **[Customer](./entities/customer.md)** - Segment, industry, account tier, headquarters location

### Product Analysis
- **[Product](./entities/product.md)** - Family, technology domain, offer type, business entity

### Partner Analysis
- **[Partner](./entities/partner.md)** - Type, tier, route to market

### Contract Analysis
- **[Contract](./entities/contract.md)** - Type, term, coverage level, auto-renew

### Sales Analysis
- **[Sales Representative](./entities/sales-representative.md)** - Role, team, covered segment

---

## Measure Relationships

### Revenue Hierarchy

```
Total Contract Value (TCV)
  └─ Annual Contract Value (ACV)
      └─ Booking Amount
          ├─ Quantity Sold
          ├─ Unit List Price
          └─ Discount Percentage
```

### Calculation Dependencies

- **Booking Amount** depends on: Quantity, Unit List Price, Discount Percentage
- **Annual Contract Value** depends on: Total Contract Value, Contract Term
- **Total Contract Value** depends on: Booking Amount, Contract Term

---

## Key Performance Indicators (KPIs)

### Primary KPIs

1. **Total Bookings** - Sum of Booking Amount USD
2. **Total ACV** - Sum of Annual Contract Value USD
3. **Total TCV** - Sum of Total Contract Value USD
4. **Average Deal Size** - Average of Booking Amount USD
5. **Average Discount** - Average of Discount Percentage
6. **Total Units Sold** - Sum of Quantity Sold

### Derived KPIs

1. **Booking Growth Rate** - Period-over-period change in Total Bookings
2. **ACV Growth Rate** - Period-over-period change in Total ACV
3. **Average Contract Term** - TCV ÷ ACV
4. **Effective Price** - Booking Amount ÷ Quantity
5. **Discount Impact** - (List Price - Booking Amount) ÷ List Price
6. **Revenue per Customer** - Total Bookings ÷ Distinct Customers

---

## Measure Catalog Summary

| Measure | Type | Aggregation | Entity | Usage |
|---------|------|-------------|--------|-------|
| Quantity Sold | Volume | SUM | Booking Transaction | Volume analysis |
| Unit List Price USD | Pricing | SUM | Booking Transaction | Pricing strategy |
| Discount Percentage | Pricing | AVG | Booking Transaction | Discount analysis |
| Booking Amount USD | Revenue | SUM | Booking Transaction | Revenue reporting |
| Annual Contract Value USD | Revenue | SUM | Booking Transaction | Recurring revenue |
| Total Contract Value USD | Revenue | SUM | Booking Transaction | Contract value |

---

## Semantic Links

- [Booking Transaction Entity](./entities/booking-transaction.md)
- [Complete Measure Catalog](./measures/index.md)
- [Entity Catalog](./entities/index.md)
- [Semantic Summary](./semantic_summary.md)
- [Main Index](./index.md)

---

## Metadata

**Catalog Type**: Business Measures  
**Domain**: Sales Bookings and Revenue Analytics  
**Total Measures**: 6  
**Source Entity**: Booking Transaction  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
