---
title: Geography
type: entity
description: Business entity representing geographic attributes for regional sales analysis
resource: entities
tags: [entity, dimension, geography, region, location, territory]
timestamp: 2026-07-28T00:00:00Z
---

# Geography

## Business Definition

Stores geographic attributes used to analyze bookings by sales region, theater, and country. The Geography entity enables regional sales analysis, market coverage evaluation, and geographic performance tracking.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_geography  
**Entity Type**: Dimension  
**Entity ID**: ENT004

---

## Attributes

- **Geography Key** (geography_key) - integer, NOT NULL
- **Sales Region** (region) - character varying(20), NULL
- **Sales Theater** (theater) - character varying(30), NULL
- **Country** (country) - character varying(40), NULL

---

## Primary Keys

- **Geography Key** (geography_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- [Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md) - Links geographies to booking transactions (One-to-Many)

---

## Measures

Geographies are analyzed using measures from related booking transactions:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)
- [Discount Percentage](../measures/discount-percentage.md)

---

## Related Concepts

### Related Entities
- [Booking Transaction](booking-transaction.md) - Booking transactions occurring in specific geographies
- [Customer](customer.md) - Customer headquarters locations
- [Partner](partner.md) - Partner geographic coverage

### Related Glossary Terms
- [Geography](../glossary/geography.md)
- [Geography Key](../glossary/geography-key.md)
- [Sales Region](../glossary/sales-region.md)
- [Sales Theater](../glossary/sales-theater.md)
- [Country](../glossary/country.md)

### Related Domains
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Uniqueness**: Each geography record is uniquely identified by Geography Key
2. **Geographic Hierarchy**: Geography follows a hierarchical structure: Region > Theater > Country
3. **Sales Region**: High-level geographic region used for executive reporting and performance analysis
4. **Sales Theater**: Subregional sales area or theater used to organize market coverage and sales operations
5. **Country**: Specific country associated with the geography record
6. **Coverage**: Geography dimension supports analysis of sales performance by market location

---

## Usage Examples

### Regional Performance Analysis
Analyze booking amounts by sales region to compare performance across major geographic markets.

### Theater-Level Analysis
Evaluate booking performance by sales theater to assess subregional market effectiveness.

### Country-Level Analysis
Analyze booking amounts and quantities by country to identify high-performing markets and expansion opportunities.

### Geographic Concentration
Identify geographic concentration of bookings to assess market diversification and risk.

### Market Penetration
Compare booking performance across geographies relative to market potential and customer base.

---

## Data Quality Notes

- Geography Key is mandatory and serves as the primary key
- Sales Region, Theater, and Country form a geographic hierarchy
- NULL values may indicate incomplete geographic classification
- Geographic attributes should align with organizational sales territory structure
- Country names should follow standardized naming conventions
- Geographic dimension should cover all active sales territories

---

## Navigation

- [View Entity Index](index.md)
- [View Related Relationships](../relationships/index.md)
- [View Related Measures](../measures/index.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Entity ID**: ENT004  
**Domain**: Sales Bookings and Revenue Analytics  
**Entity Type**: Dimension  
**Attribute Count**: 4  
**Relationship Count**: 1  
**Last Updated**: 2026-07-28T00:00:00Z
