---
title: Contract
type: entity
description: Business entity representing commercial agreements associated with bookings
resource: entities
tags: [entity, dimension, contract, agreement, terms]
timestamp: 2026-07-28T00:00:00Z
---

# Contract

## Business Definition

Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level. The Contract entity enables analysis of booking performance by contract characteristics and supports contract lifecycle management.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_contract  
**Entity Type**: Dimension  
**Entity ID**: ENT001

---

## Attributes

- **Contract Key** (contract_key) - integer, NOT NULL
- **Contract Type** (contract_type) - character varying(40), NULL
- **Contract Term Months** (term_months) - integer, NULL
- **Auto Renew Flag** (auto_renew_flag) - character(1), NULL
- **Coverage Level** (coverage_level) - character varying(20), NULL

---

## Primary Keys

- **Contract Key** (contract_key)

---

## Foreign Keys

None

---

## Relationships

### Outgoing Relationships

- [Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md) - Links contracts to booking transactions (One-to-Many)

---

## Measures

Contracts are analyzed using measures from related booking transactions:

- [Booking Amount USD](../measures/booking-amount-usd.md)
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md)
- [Total Contract Value USD](../measures/total-contract-value-usd.md)
- [Quantity Sold](../measures/quantity-sold.md)

---

## Related Concepts

### Related Entities
- [Booking Transaction](booking-transaction.md) - Booking transactions associated with this contract
- [Customer](customer.md) - Customers who enter into contracts
- [Product](product.md) - Products covered by contracts

### Related Glossary Terms
- [Contract](../glossary/contract.md)
- [Contract Key](../glossary/contract-key.md)
- [Contract Type](../glossary/contract-type.md)
- [Contract Term Months](../glossary/contract-term-months.md)
- [Auto Renew Flag](../glossary/auto-renew-flag.md)
- [Coverage Level](../glossary/coverage-level.md)

### Related Domains
- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Business Rules

1. **Uniqueness**: Each contract record is uniquely identified by Contract Key
2. **Contract Term**: Contract term is measured in months and determines the duration of the agreement
3. **Auto Renewal**: Auto Renew Flag indicates whether the contract automatically renews at term end
4. **Coverage**: Coverage Level describes the service or support tier provided under the contract
5. **Contract Types**: Common contract types include SaaS subscription, Enterprise Agreement, and support contracts

---

## Usage Examples

### Analysis by Contract Type
Analyze booking amounts and contract values by contract type to understand which agreement structures drive the most revenue.

### Renewal Analysis
Use Auto Renew Flag to track adoption of automatic renewal terms and predict future revenue streams.

### Contract Term Analysis
Analyze average contract terms by customer segment and product family to optimize contract structures.

### Coverage Analysis
Evaluate booking performance by coverage level to understand demand for different service tiers.

---

## Data Quality Notes

- Contract Key is mandatory and serves as the primary key
- Descriptive attributes (Contract Type, Coverage Level) may be NULL for incomplete records
- Contract Term Months should be positive when populated
- Auto Renew Flag typically uses 'Y' or 'N' values

---

## Navigation

- [View Entity Index](index.md)
- [View Related Relationships](../relationships/index.md)
- [View Related Measures](../measures/index.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Entity ID**: ENT001  
**Domain**: Sales Bookings and Revenue Analytics  
**Entity Type**: Dimension  
**Attribute Count**: 5  
**Relationship Count**: 1  
**Last Updated**: 2026-07-28T00:00:00Z
