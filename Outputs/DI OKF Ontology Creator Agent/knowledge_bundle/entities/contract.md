---
title: Contract
type: entity
id: ENT001
domain: Sales Bookings and Revenue Analytics
technical_table: QuoteToBooking.dim_contract
business_keys:
  - contract_key
version: 1.0
status: generated
---

# Contract

## Business Definition

Stores the contractual attributes associated with a booking, including agreement type, duration, renewal behavior, and support or service coverage level.

## Technical Mapping

- Table: `QuoteToBooking.dim_contract`
- Primary business key(s): `contract_key`

## Attributes

| Attribute | Technical Column | Data Type | Nullable | PK | FK | Description |
| --- | --- | --- | --- | --- | --- | --- |
| Contract Key | contract_key | integer | No | Yes | No | Surrogate key that uniquely identifies a contract record in the contract dimension. |
| Contract Type | contract_type | character varying | Yes | No | No | Indicates the type of commercial agreement or service contract associated with the booking, such as SaaS Subscription or Enterprise Agreement. |
| Contract Term Months | term_months | integer | Yes | No | No | Specifies the duration of the contract in months. |
| Auto Renew Indicator | auto_renew_flag | character | Yes | No | No | Indicates whether the contract is configured to renew automatically. |
| Coverage Level | coverage_level | character varying | Yes | No | No | Describes the support, service, or entitlement coverage level provided under the contract. |

## Keys

- Primary Key: `contract_key`
- Referenced by: [Booking Transaction](booking-transaction.md)

## Measures

- No direct measures defined for this entity.

## Relationships

- Parent in [Contract to Booking Transaction](../relationships/contract-to-booking-transaction.md)

## Related Concepts

- [Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
- [Booking Transaction](booking-transaction.md)
- [Contract](../glossary/contract.md)
- [Coverage Level](../glossary/coverage-level.md)