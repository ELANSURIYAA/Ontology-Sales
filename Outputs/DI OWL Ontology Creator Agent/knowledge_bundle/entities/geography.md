---
title: Geography
type: entity
description: Geographic attributes used to analyze bookings by sales region, theater, and country
resource: entities
tags: [geography, location, region, dimension, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Geography

## Business Definition

The Geography entity stores geographic attributes used to analyze bookings by sales region, theater, and country. It provides hierarchical geographic context for sales performance analysis across global markets. This entity enables regional analysis, territory management, and geographic market segmentation.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_geography  
**Source Schema**: QuoteToBooking  
**Entity Type**: Dimension  
**Entity ID**: ENT004

---

## Attributes

- **Geography Key** - Surrogate key that uniquely identifies a geography record in the geography dimension
- **Sales Region** - High-level geographic region used for reporting and performance analysis
- **Sales Theater** - Subregional sales area or theater used to organize market coverage and reporting
- **Country** - Country associated with the geography record

---

## Primary Keys

- **Geography Key** (geography_key) - Surrogate key, Integer, Not Nullable

---

## Foreign Keys

None - This is a dimension entity

---

## Relationships

### Outgoing Relationships

- **[Geography to Booking Transaction](../relationships/geography-to-booking-transaction.md)** - One-to-Many relationship linking geographies to booking transactions

### Related Entities

- **[Booking Transaction](./booking-transaction.md)** - Fact entity containing booking records with geographic context
- **[Customer](./customer.md)** - Customers with headquarters locations
- **[Sales Representative](./sales-representative.md)** - Sales personnel assigned to territories

---

## Measures

Geographies support regional analysis of all measures:

- **[Booking Amount USD](../measures/booking-amount-usd.md)** - Revenue by region, theater, and country
- **[Annual Contract Value USD](../measures/annual-contract-value-usd.md)** - ACV by geographic market
- **[Total Contract Value USD](../measures/total-contract-value-usd.md)** - TCV by territory
- **[Quantity Sold](../measures/quantity-sold.md)** - Volume by geographic area
- **[Discount Percentage](../measures/discount-percentage.md)** - Regional pricing patterns
- **[Unit List Price USD](../measures/unit-list-price-usd.md)** - Price positioning by market

---

## Business Rules

1. Geography Key must be unique and not null
2. Country must be valid ISO country code
3. Sales Theater must belong to parent Sales Region
4. Geographic hierarchy must be consistent (Region → Theater → Country)
5. Each country must map to exactly one theater and region
6. Sales Region must be from approved list of global regions

---

## Analytical Usage

### Regional Analysis
- Compare booking performance across major global regions
- Track regional growth rates and market share
- Analyze regional revenue contribution

### Theater Analysis
- Evaluate subregional sales theater performance
- Compare theater-level booking patterns
- Track theater coverage and penetration

### Country Analysis
- Analyze country-specific booking performance
- Identify high-performing and emerging markets
- Track country-level market share

### Geographic Trends
- Monitor geographic expansion and growth
- Identify regional opportunities and challenges
- Track market penetration by geography

---

## Geographic Hierarchy

```
Sales Region
  └─ Sales Theater
      └─ Country
```

### Example Hierarchy
```
Americas
  ├─ North America
  │   ├─ United States
  │   ├─ Canada
  │   └─ Mexico
  └─ Latin America
      ├─ Brazil
      └─ Argentina

EMEA
  ├─ Europe
  │   ├─ United Kingdom
  │   ├─ Germany
  │   └─ France
  └─ Middle East
      └─ United Arab Emirates

APAC
  ├─ Asia Pacific North
  │   ├─ Japan
  │   └─ South Korea
  └─ Asia Pacific South
      ├─ Australia
      └─ Singapore
```

---

## Related Concepts

- **[Customer](./customer.md)** - Customer headquarters locations
- **[Sales Representative](./sales-representative.md)** - Territory assignments
- **[Partner](./partner.md)** - Partner geographic coverage
- **[Booking Transaction](./booking-transaction.md)** - Transaction locations

---

## Glossary Terms

- [Geography](../glossary/geography.md)
- [Geography Key](../glossary/geography-key.md)
- [Sales Region](../glossary/sales-region.md)
- [Sales Theater](../glossary/sales-theater.md)
- [Country](../glossary/country.md)

---

## Attribute Details

| Attribute | Technical Column | Data Type | Nullable | Key Type | Description |
|-----------|-----------------|-----------|----------|----------|-------------|
| Geography Key | geography_key | integer | No | Primary | Surrogate key uniquely identifying geography |
| Sales Region | region | character varying(20) | Yes | - | High-level geographic region |
| Sales Theater | theater | character varying(30) | Yes | - | Subregional sales area |
| Country | country | character varying(40) | Yes | - | Country designation |

---

## Semantic Links

- [Entity Index](./index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Relationship Index](../relationships/index.md)
- [Measure Index](../measures/index.md)
- [Main Index](../index.md)

---

## Metadata

**Entity ID**: ENT004  
**Domain ID**: DOM001  
**Entity Type**: Dimension  
**Technical Table**: QuoteToBooking.dim_geography  
**Total Attributes**: 4  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
