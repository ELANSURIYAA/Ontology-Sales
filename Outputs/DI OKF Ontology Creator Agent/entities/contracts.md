---
title: Contracts
type: entity
description: Describes the commercial agreement or service coverage terms associated with a booking, including contract type, duration, renewal behavior, and support coverage level
resource: entities
tags: [contracts, dimension, contract-type, coverage]
timestamp: 2026-07-28T00:00:00Z
---

# Contracts

## Business Definition

The Contracts entity represents the dimension table that describes the commercial agreement or service coverage terms associated with a booking. Each record contains contract type classifications, term duration specifications, renewal behavior indicators, and support coverage level designations. This entity enables analysis of booking transactions by contract characteristics and supports contract management and renewal strategies.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_contract

**Source Schema**: quotetobooking

**Entity Type**: Dimension Table

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

None

---

## Relationships

- [Bookings to Contracts](../relationships/bookings-to-contracts.md)

---

## Measures

All booking-related measures can be analyzed by contract attributes:
- [Booking Count](../measures/booking-count.md)
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md)
- [Total ACV USD](../measures/total-acv-usd.md)
- [Total TCV USD](../measures/total-tcv-usd.md)
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md)

---

## Related Concepts

- [Annual Contract Value](../glossary/annual-contract-value.md)
- [Total Contract Value](../glossary/total-contract-value.md)
- [Renewal](../glossary/renewal.md)
- [Booking Transaction](../glossary/booking-transaction.md)

---

## Business Rules

1. **Unique Contract Key**: Each contract record must have a unique contract_key
2. **Contract Type Classification**: Contracts are classified by type such as Enterprise Agreement, SaaS Subscription, or Solution Support
3. **Term Duration**: Contract term is specified in months
4. **Auto-Renewal Indicator**: Flag indicates whether the contract automatically renews at term end
5. **Coverage Level**: Service or support coverage level is specified for each contract

---

## Attribute Definitions

### contract_key
Surrogate key that uniquely identifies a contract record in the contract dimension. Used as the primary key and referenced by the bookings fact table.

### contract_type
Type of commercial agreement or support entitlement, such as Enterprise Agreement, SaaS Subscription, or Solution Support. Enables contract type analysis and revenue model tracking.

### term_months
Number of months covered by the contract or subscription term. Used to calculate annualized values and track contract duration patterns.

### auto_renew_flag
Indicator showing whether the contract is set to renew automatically at the end of its term. Used to forecast renewal revenue and manage renewal processes.

### coverage_level
Service or support coverage level provided under the contract. Enables coverage level analysis and service tier tracking.

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)

---

## Usage Examples

### Contract Type Analysis
- Analyze booking amount by contract type
- Track subscription vs perpetual license revenue
- Monitor contract type mix and trends

### Term Duration Analysis
- Analyze average contract term length
- Track term duration trends over time
- Evaluate impact of term length on ACV and TCV

### Auto-Renewal Analysis
- Track percentage of contracts with auto-renewal
- Forecast renewal revenue based on auto-renew flag
- Optimize renewal processes and customer retention

### Coverage Level Analysis
- Analyze booking distribution by coverage level
- Track premium vs standard coverage adoption
- Optimize service tier offerings

---

## Data Quality Checks

- contract_key is unique and not null
- contract_type is not null and is a valid type
- term_months is positive and not null
- auto_renew_flag is either 0 or 1
- coverage_level is a valid coverage designation
