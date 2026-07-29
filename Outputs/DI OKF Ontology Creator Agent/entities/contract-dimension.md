---
title: Contract Dimension
type: entity
description: Contract and service agreement attributes used to classify bookings
resource: entities
tags: [okf, entity, contract, dimension, contract-management]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Dimension

## Business Definition

The Contract Dimension stores contract and service agreement attributes used to classify bookings by contract type, term, renewal behavior, and coverage level. This dimension enables analysis of booking performance across different contract characteristics and supports renewal forecasting and contract lifecycle management.

---

## Technical Mapping

**Source Schema**: quotetobooking  
**Source Table**: dim_contract  
**Entity Type**: Dimension  
**Grain**: One record per unique contract configuration

---

## Attributes

- contract_key
- contract_type
- term_months
- auto_renew_flag
- coverage_level

---

## Primary Keys

- contract_key

---

## Foreign Keys

None (this is a dimension table)

---

## Relationships

### Outbound Relationships
- [Contract to Booking](../relationships/contract-to-booking.md) - One-to-Many relationship to Booking Fact

---

## Measures

All booking measures can be analyzed by contract attributes:

- [Quantity Sold](../measures/quantity-sold.md)
- [Unit List Price USD](../measures/unit-list-price-usd.md)
- [Discount Percentage](../measures/discount-percentage.md)
- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)

---

## Related Concepts

### Related Entities
- [Booking Fact](booking-fact.md)

### Related Domains
- [Contract Management](../domains/contract-management.md)
- [Sales Transactions](../domains/sales-transactions.md)
- [Revenue Metrics](../domains/revenue-metrics.md)

### Related Glossary Terms
- [Contract Dimension](../glossary/contract-dimension.md)
- [Contract Key](../glossary/contract-key.md)
- [Contract Type](../glossary/contract-type.md)
- [Contract Term Months](../glossary/contract-term-months.md)
- [Auto Renew Flag](../glossary/auto-renew-flag.md)
- [Coverage Level](../glossary/coverage-level.md)

---

## Business Rules

1. Contract Key must be unique and not null
2. Contract Type should be populated for all records
3. Contract Term Months must be a positive integer
4. Auto Renew Flag must be 'Y' or 'N'
5. Coverage Level should match approved coverage level values
6. Contract attributes must remain consistent for a given contract key

---

## Attribute Details

### contract_key
- **Data Type**: integer
- **Nullable**: No
- **Primary Key**: Yes
- **Description**: Surrogate key that uniquely identifies a contract record in the contract dimension

### contract_type
- **Data Type**: character varying(40)
- **Nullable**: Yes
- **Description**: Type of commercial agreement associated with the booking, such as Enterprise Agreement, SaaS Subscription, or support contract

### term_months
- **Data Type**: integer
- **Nullable**: Yes
- **Description**: Number of months covered by the contract or service agreement

### auto_renew_flag
- **Data Type**: character(1)
- **Nullable**: Yes
- **Description**: Indicator showing whether the contract is configured to renew automatically

### coverage_level
- **Data Type**: character varying(20)
- **Nullable**: Yes
- **Description**: Service or support coverage level provided under the contract

---

## Analytical Use Cases

- Analyze bookings by contract type
- Track contract term distribution
- Monitor auto-renewal rates
- Evaluate coverage level mix
- Support renewal forecasting
- Measure contract performance

---

## Data Quality Metrics

- **Completeness**: Contract Key must be 100% populated
- **Uniqueness**: Contract Key must be unique
- **Validity**: Contract Type must match approved values
- **Consistency**: Contract attributes must align with business rules

---

## Navigation

- [Back to Entities Index](index.md)
- [Back to Bundle Index](../index.md)
