---
title: Metrics Catalog
type: index
description: Comprehensive catalog of business measures and key performance indicators
resource: knowledge_bundle
tags: [okf, metrics, measures, kpi, quote-to-booking]
timestamp: 2026-07-28T00:00:00Z
---

# Metrics Catalog

## Overview

This catalog documents all business measures and key performance indicators (KPIs) available in the Quote to Booking semantic model. These metrics enable comprehensive analysis of sales performance, revenue recognition, pricing effectiveness, and booking volume.

---

## Measure Categories

### Volume Metrics
Measures related to booking quantities and transaction volumes.

### Pricing Metrics
Measures related to list prices and discount structures.

### Revenue Metrics
Measures related to booked revenue and contract values.

---

## Core Measures

### [Quantity Sold](measures/quantity-sold.md)
- **Type**: Volume Metric
- **Aggregation**: Sum
- **Description**: Number of units, licenses, or subscriptions booked in the transaction
- **Business Use**: Track booking volume, analyze product demand, measure sales velocity

### [Unit List Price USD](measures/unit-list-price-usd.md)
- **Type**: Pricing Metric
- **Aggregation**: Average
- **Description**: Standard list price per unit in U.S. dollars before discounts
- **Business Use**: Analyze pricing strategies, compare product pricing, track price changes

### [Discount Percentage](measures/discount-percentage.md)
- **Type**: Pricing Metric
- **Aggregation**: Average
- **Description**: Discount applied to the list price for the booking line
- **Business Use**: Monitor discount trends, analyze pricing pressure, evaluate margin impact

### [Booking Amount USD](measures/booking-amount-usd.md)
- **Type**: Revenue Metric
- **Aggregation**: Sum
- **Description**: Total booked revenue amount in U.S. dollars for the transaction
- **Business Use**: Track total revenue, measure sales performance, analyze revenue trends

### [Annual Contract Value USD](measures/annual-contract-value-usd.md)
- **Type**: Revenue Metric
- **Aggregation**: Sum
- **Description**: Annualized contract value in U.S. dollars used for recurring revenue analysis
- **Business Use**: Measure recurring revenue, analyze subscription performance, forecast annual revenue

### [Total Contract Value USD](measures/total-contract-value-usd.md)
- **Type**: Revenue Metric
- **Aggregation**: Sum
- **Description**: Total contract value in U.S. dollars over the full contract term
- **Business Use**: Analyze long-term contract value, measure deal size, evaluate contract profitability

---

## Measure Relationships

### Volume to Revenue
- **Quantity Sold** × **Unit List Price USD** × (1 - **Discount Percentage**) = **Booking Amount USD**

### Revenue Decomposition
- **Booking Amount USD**: Total transaction value
- **Annual Contract Value USD**: Annualized recurring portion
- **Total Contract Value USD**: Full contract term value

---

## Analytical Dimensions

All measures can be analyzed across the following dimensions:

### Customer Dimensions
- Customer Name
- Customer Segment
- Industry
- Account Tier
- Headquarters Country
- Headquarters Region

### Product Dimensions
- Product Name
- Product Family
- Technology Domain
- Offer Type
- Business Entity

### Partner Dimensions
- Partner Name
- Partner Type
- Partner Tier
- Route to Market

### Geographic Dimensions
- Region
- Theater
- Country

### Sales Dimensions
- Sales Representative Name
- Sales Role
- Sales Team
- Segment Covered

### Contract Dimensions
- Contract Type
- Contract Term Months
- Auto Renew Flag
- Coverage Level

### Time Dimensions
- Full Date
- Month Name
- Calendar Year
- Fiscal Year
- Fiscal Quarter
- Fiscal Period Sequence

### Transaction Dimensions
- Booking Type
- Renewal Indicator
- Order Number
- Order Line Number

---

## Key Performance Indicators (KPIs)

### Sales Performance KPIs
- Total Booking Amount
- Average Deal Size (Booking Amount / Count of Bookings)
- Booking Growth Rate (Period over Period)
- New Business vs Renewal Mix

### Volume KPIs
- Total Quantity Sold
- Average Quantity per Booking
- Volume Growth Rate

### Pricing KPIs
- Average Unit List Price
- Average Discount Percentage
- Effective Price (List Price × (1 - Discount %))
- Price Realization Rate

### Revenue KPIs
- Total Annual Contract Value
- Total Contract Value
- ACV to TCV Ratio
- Revenue per Customer
- Revenue per Product
- Revenue per Sales Representative

### Contract KPIs
- Average Contract Term
- Auto Renew Rate
- Contract Value by Type
- Coverage Level Distribution

---

## Measure Hierarchies

### Revenue Hierarchy
```
Total Contract Value USD
└── Annual Contract Value USD
    └── Booking Amount USD
```

### Pricing Hierarchy
```
Booking Amount USD
├── Unit List Price USD
├── Discount Percentage
└── Quantity Sold
```

---

## Calculation Rules

### Aggregation Rules
- **Sum Measures**: Quantity Sold, Booking Amount USD, Annual Contract Value USD, Total Contract Value USD
- **Average Measures**: Unit List Price USD, Discount Percentage

### Filtering Rules
- All measures respect dimensional filters
- Time-based measures respect fiscal calendar
- Revenue measures exclude cancelled bookings (if applicable)

### Granularity Rules
- **Atomic Grain**: Individual booking transaction line
- **Aggregation Levels**: Customer, Product, Partner, Geography, Sales Rep, Contract, Time

---

## Measure Metadata

| Measure | Entity | Technical Column | Data Type | Nullable | Business Owner |
|---------|--------|------------------|-----------|----------|----------------|
| Quantity Sold | Booking Fact | quantity | integer | Yes | Sales Operations |
| Unit List Price USD | Booking Fact | unit_list_price_usd | numeric(12,2) | Yes | Pricing Team |
| Discount Percentage | Booking Fact | discount_pct | numeric(5,2) | Yes | Pricing Team |
| Booking Amount USD | Booking Fact | booking_amount_usd | numeric(14,2) | Yes | Finance |
| Annual Contract Value USD | Booking Fact | acv_usd | numeric(14,2) | Yes | Finance |
| Total Contract Value USD | Booking Fact | tcv_usd | numeric(14,2) | Yes | Finance |

---

## Data Quality Rules

### Validation Rules
- Quantity Sold must be greater than 0
- Unit List Price USD must be greater than or equal to 0
- Discount Percentage must be between 0 and 100
- Booking Amount USD must be greater than or equal to 0
- Annual Contract Value USD must be greater than or equal to 0
- Total Contract Value USD must be greater than or equal to Annual Contract Value USD

### Consistency Rules
- Booking Amount should align with (Quantity × Unit List Price × (1 - Discount %))
- Total Contract Value should be greater than or equal to Annual Contract Value
- Annual Contract Value should reflect contract term normalization

---

## Usage Guidelines

### Reporting Best Practices
1. Always specify time period for trending analysis
2. Use appropriate aggregation level for business question
3. Apply dimensional filters to focus analysis
4. Compare metrics across consistent time periods
5. Validate measure calculations against source systems

### Common Analysis Patterns
- **Trend Analysis**: Measure performance over time periods
- **Comparative Analysis**: Compare measures across dimensions
- **Contribution Analysis**: Calculate percentage contribution to totals
- **Variance Analysis**: Analyze actual vs target or period over period
- **Cohort Analysis**: Track measure performance by customer or product cohorts

---

## Related Resources

- [Booking Fact Entity](entities/booking-fact.md)
- [Complete Measure Documents](measures/index.md)
- [Semantic Summary](semantic_summary.md)
- [Business Glossary](glossary/index.md)
