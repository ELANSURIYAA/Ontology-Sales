---
title: Contract Management Domain
type: domain
description: Contract and service agreement attributes used to classify bookings by contract type, term, renewal behavior, and coverage level
resource: domains
tags: [okf, domain, contract-management, contract, agreement]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Management Domain

## Business Definition

The Contract Management domain encompasses contract and service agreement attributes used to classify bookings by contract type, term, renewal behavior, and coverage level. This domain provides the contractual context necessary for contract analytics and renewal management.

---

## Business Purpose

This domain enables business users to:

- Analyze bookings by contract type
- Track contract term distributions
- Monitor auto-renewal rates
- Evaluate coverage level mix
- Support renewal forecasting
- Measure contract performance
- Enable contract lifecycle management

---

## Domain Scope

### Included
- Contract type classifications
- Contract term durations
- Auto-renewal indicators
- Service coverage levels
- Contract descriptive attributes

### Excluded
- Detailed contract terms and conditions
- Contract pricing and discounting (covered in Pricing domain)
- Contract legal language
- Contract approval workflows
- Contract documents and attachments

---

## Related Entities

### Primary Entities
- [Contract Dimension](../entities/contract-dimension.md)

---

## Related Measures

All sales and revenue measures can be analyzed by contract attributes:

- [Quantity Sold](../measures/quantity-sold.md) by contract
- [Booking Amount USD](../measures/booking-amount-usd.md) by contract
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md) by contract
- [Total Contract Value USD](../measures/total-contract-value-usd.md) by contract
- [Unit List Price USD](../measures/unit-list-price-usd.md) by contract
- [Discount Percentage](../measures/discount-percentage.md) by contract

---

## Related Relationships

- [Contract to Booking](../relationships/contract-to-booking.md)

---

## Key Business Concepts

### Contract Type
Type of commercial agreement associated with the booking, such as:
- **Enterprise Agreement**: Large-scale enterprise licensing agreements
- **SaaS Subscription**: Cloud-based software as a service subscriptions
- **Software Subscription**: On-premise or hybrid software subscriptions
- **Support Contract**: Maintenance and support agreements
- **Professional Services**: Consulting and implementation services agreements

### Contract Term
Number of months covered by the contract or service agreement. Common terms include:
- 12 months (1 year)
- 24 months (2 years)
- 36 months (3 years)
- 60 months (5 years)

### Auto Renew Flag
Indicator showing whether the contract is configured to renew automatically at the end of the term, supporting renewal forecasting and customer retention analysis.

### Coverage Level
Service or support coverage level provided under the contract, such as:
- Basic
- Standard
- Premium
- 24x7 Support
- Mission Critical

---

## Business Rules

1. Every contract record must have a unique Contract Key (surrogate key)
2. Contract Type should be populated for all contracts
3. Contract Term Months should be greater than 0
4. Auto Renew Flag should be 'Y' (Yes) or 'N' (No)
5. Coverage Level should match approved coverage level values
6. Contract attributes should align with contract terms and conditions

---

## Analytical Use Cases

### Contract Type Analysis
- Compare revenue and bookings across contract types
- Analyze contract type mix and trends
- Track subscription versus perpetual license adoption
- Evaluate contract type profitability

### Contract Term Analysis
- Analyze distribution of contract terms
- Track average contract term trends
- Compare short-term versus long-term contracts
- Support contract term optimization strategies

### Renewal Analysis
- Monitor auto-renewal rates
- Forecast renewal revenue
- Identify renewal risk and opportunities
- Track renewal conversion rates

### Coverage Level Analysis
- Analyze coverage level mix
- Track premium versus standard coverage adoption
- Evaluate coverage level pricing and profitability
- Support coverage level strategy

### Contract Lifecycle Management
- Track contract start and end dates
- Monitor contract expiration and renewal timing
- Analyze contract value over lifecycle
- Support proactive renewal management

---

## Data Quality Metrics

### Completeness
- Contract Key must be populated for all records
- Contract Type should be populated (>95% target)
- Contract Term Months should be populated (>90% target)
- Auto Renew Flag should be populated (>90% target)

### Accuracy
- Contract Key must be unique
- Contract Type must match approved type values
- Contract Term Months must be positive integer
- Auto Renew Flag must be 'Y' or 'N'
- Coverage Level must match approved level values

### Consistency
- Contract attributes must be consistent across all bookings
- Contract master data must reconcile with source contract systems
- Contract terms must align with business rules

---

## Technical Implementation

### Source System
- **Schema**: quotetobooking
- **Table**: dim_contract
- **Primary Key**: contract_key (surrogate key)
- **Type**: Slowly Changing Dimension (Type 1 or Type 2)

### Key Attributes
- Contract Key (Primary Key)
- Contract Type
- Contract Term Months
- Auto Renew Flag
- Coverage Level

---

## Semantic Links

### Related Domains
- [Sales Transactions](sales-transactions.md)
- [Revenue Metrics](revenue-metrics.md)
- [Customer Management](customer-management.md)
- [Product Management](product-management.md)

### Related Glossary Terms
- [Contract Dimension](../glossary/contract-dimension.md)
- [Contract Key](../glossary/contract-key.md)
- [Contract Type](../glossary/contract-type.md)
- [Contract Term Months](../glossary/contract-term-months.md)
- [Auto Renew Flag](../glossary/auto-renew-flag.md)
- [Coverage Level](../glossary/coverage-level.md)

---

## Navigation

- [Back to Domains Index](index.md)
- [Back to Bundle Index](../index.md)
