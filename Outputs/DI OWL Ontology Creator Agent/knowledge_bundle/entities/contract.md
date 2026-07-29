---
title: Contract
type: entity
description: Commercial agreements associated with bookings including contract type, term, renewal behavior, and support coverage level
resource: entities
tags: [contract, agreement, dimension, entity]
timestamp: 2026-07-28T00:00:00Z
---

# Contract

## Business Definition

The Contract entity stores the business attributes of commercial agreements associated with bookings. It captures essential contract characteristics including contract type, term duration, renewal behavior, and support coverage level. This entity enables analysis of booking performance by contract attributes and supports contract management and renewal tracking.

---

## Technical Mapping

**Source Table**: QuoteToBooking.dim_contract  
**Source Schema**: QuoteToBooking  
**Entity Type**: Dimension  
**Entity ID**: ENT001

---

## Attributes

- **Contract Key** - Surrogate key that uniquely identifies a contract record in the contract dimension
- **Contract Type** - Describes the type of commercial agreement attached to the booking, such as SaaS subscription, Enterprise Agreement, or support contract
- **Contract Term Months** - Indicates the duration of the contract in months
- **Auto Renew Flag** - Indicates whether the contract is set to renew automatically at the end of its term
- **Coverage Level** - Describes the level of service or support coverage provided under the contract

---

## Primary Keys

- **Contract Key** (contract_key) - Surrogate key, Integer, Not Nullable

---

## Foreign Keys

None - This is a dimension entity

---

## Relationships

### Outgoing Relationships

- **[Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)** - One-to-Many relationship linking contracts to booking transactions

### Related Entities

- **[Booking Transaction](./booking-transaction.md)** - Fact entity containing booking records associated with contracts

---

## Measures

Contracts support analysis of the following measures:

- **[Booking Amount USD](../measures/booking-amount-usd.md)** - Total booked revenue by contract type and term
- **[Annual Contract Value USD](../measures/annual-contract-value-usd.md)** - ACV by contract attributes
- **[Total Contract Value USD](../measures/total-contract-value-usd.md)** - TCV by contract characteristics
- **[Quantity Sold](../measures/quantity-sold.md)** - Volume by contract type
- **[Discount Percentage](../measures/discount-percentage.md)** - Pricing by contract terms

---

## Business Rules

1. Contract Key must be unique and not null
2. Contract Term Months must be a positive integer
3. Auto Renew Flag must be 'Y' or 'N'
4. Coverage Level must be from approved list of service levels
5. Contract Type must be from approved list of agreement types

---

## Analytical Usage

### Contract Type Analysis
- Compare booking performance across SaaS subscriptions, Enterprise Agreements, and support contracts
- Analyze contract type mix and trends over time
- Evaluate revenue contribution by contract type

### Contract Term Analysis
- Analyze booking distribution by contract duration
- Track average contract term trends
- Compare short-term vs long-term contract performance

### Renewal Analysis
- Monitor auto-renewal rates and patterns
- Identify renewal opportunities
- Track renewal vs new business mix

### Coverage Analysis
- Analyze booking performance by support coverage level
- Evaluate premium vs standard coverage adoption
- Track coverage level trends and preferences

---

## Related Concepts

- **[Customer](./customer.md)** - Customers who enter into contracts
- **[Product](./product.md)** - Products and services covered by contracts
- **[Sales Representative](./sales-representative.md)** - Sales personnel managing contract relationships
- **[Date](./date.md)** - Contract effective dates and renewal dates
- **[Booking Transaction](./booking-transaction.md)** - Transactions associated with contracts

---

## Glossary Terms

- [Contract](../glossary/contract.md)
- [Contract Key](../glossary/contract-key.md)
- [Contract Type](../glossary/contract-type.md)
- [Contract Term Months](../glossary/contract-term-months.md)
- [Auto Renew Flag](../glossary/auto-renew-flag.md)
- [Coverage Level](../glossary/coverage-level.md)

---

## Attribute Details

| Attribute | Technical Column | Data Type | Nullable | Key Type | Description |
|-----------|-----------------|-----------|----------|----------|-------------|
| Contract Key | contract_key | integer | No | Primary | Surrogate key that uniquely identifies a contract record |
| Contract Type | contract_type | character varying(40) | Yes | - | Type of commercial agreement |
| Contract Term Months | term_months | integer | Yes | - | Duration of the contract in months |
| Auto Renew Flag | auto_renew_flag | character(1) | Yes | - | Indicates automatic renewal setting |
| Coverage Level | coverage_level | character varying(20) | Yes | - | Level of service or support coverage |

---

## Semantic Links

- [Entity Index](./index.md)
- [Domain: Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Relationship Index](../relationships/index.md)
- [Measure Index](../measures/index.md)
- [Main Index](../index.md)

---

## Metadata

**Entity ID**: ENT001  
**Domain ID**: DOM001  
**Entity Type**: Dimension  
**Technical Table**: QuoteToBooking.dim_contract  
**Total Attributes**: 5  
**Format**: Open Knowledge Format (OKF)  
**Version**: 1.0  
**Generated**: 2026-07-28T00:00:00Z
