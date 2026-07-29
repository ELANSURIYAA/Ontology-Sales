---
title: Sales Organization Domain
type: domain
description: Sales representative and organizational attributes used to analyze bookings by seller, role, team, and covered segment
resource: domains
tags: [okf, domain, sales-organization, sales-rep, team]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Organization Domain

## Business Definition

The Sales Organization domain encompasses sales representative and organizational attributes used to analyze bookings by seller, role, team, and covered segment. This domain provides the sales organizational context necessary for sales performance management and territory analytics.

---

## Business Purpose

This domain enables business users to:

- Analyze sales performance by sales representative
- Track revenue by sales role and team
- Monitor quota attainment and productivity
- Evaluate segment coverage effectiveness
- Support sales capacity planning
- Measure sales representative contribution
- Enable sales compensation and incentive analysis

---

## Domain Scope

### Included
- Sales representative identity and identification
- Sales role classifications
- Sales team assignments
- Segment coverage assignments
- Sales representative descriptive attributes

### Excluded
- Sales representative compensation details
- Sales quotas and targets
- Sales representative contact information
- Sales representative employment history
- Sales representative performance reviews

---

## Related Entities

### Primary Entities
- [Sales Representative Dimension](../entities/sales-representative-dimension.md)

---

## Related Measures

All sales and revenue measures can be analyzed by sales representative attributes:

- [Quantity Sold](../measures/quantity-sold.md) by sales representative
- [Booking Amount USD](../measures/booking-amount-usd.md) by sales representative
- [Annual Contract Value USD](../measures/annual-contract-value-usd.md) by sales representative
- [Total Contract Value USD](../measures/total-contract-value-usd.md) by sales representative
- [Unit List Price USD](../measures/unit-list-price-usd.md) by sales representative
- [Discount Percentage](../measures/discount-percentage.md) by sales representative

---

## Related Relationships

- [Sales Representative to Booking](../relationships/sales-representative-to-booking.md)

---

## Key Business Concepts

### Sales Representative
Individual sales person responsible for managing customer accounts, opportunities, and booking transactions. Each representative is uniquely identified and tracked for performance management.

### Sales Role
Job role or selling role performed by the sales representative, such as:
- Account Executive
- Account Manager
- Inside Sales Representative
- Sales Engineer
- Territory Manager
- Channel Account Manager

### Sales Team
Sales team or organization to which the representative belongs, enabling team-level performance tracking and management.

### Segment Covered
Customer segment primarily covered by the sales representative, such as:
- Enterprise
- Service Provider
- Public Sector
- Commercial
- Small Business

---

## Business Rules

1. Every sales representative must have a unique Sales Representative Key (surrogate key)
2. Every sales representative must have a unique Sales Representative ID (business key)
3. Sales Representative Name is required for reporting and analysis
4. Sales Role should be populated for all representatives
5. Sales Team should be populated for all representatives
6. Segment Covered should align with customer segment classifications
7. Sales representative assignments should be current and accurate

---

## Analytical Use Cases

### Sales Representative Performance
- Track individual sales representative revenue and bookings
- Identify top performing sales representatives
- Analyze sales representative productivity metrics
- Monitor quota attainment by representative

### Sales Role Analysis
- Compare performance across sales roles
- Analyze role-specific productivity and effectiveness
- Support role-based capacity planning
- Evaluate role specialization strategies

### Sales Team Analysis
- Track team-level revenue and bookings
- Compare team performance
- Analyze team composition and structure
- Support team-based incentive programs

### Segment Coverage Analysis
- Analyze coverage by customer segment
- Identify segment coverage gaps
- Evaluate segment specialization effectiveness
- Support territory and coverage planning

### Sales Capacity Planning
- Analyze sales representative workload and capacity
- Track representative-to-customer ratios
- Support hiring and resource allocation decisions
- Evaluate territory balance and optimization

---

## Data Quality Metrics

### Completeness
- Sales Representative Key must be populated for all records
- Sales Representative ID must be populated for all records
- Sales Representative Name must be populated for all records
- Sales Role should be populated (>95% target)
- Sales Team should be populated (>95% target)

### Accuracy
- Sales Representative ID must be unique
- Sales Role must match approved role values
- Sales Team must match organizational structure
- Segment Covered must match approved segment values
- Sales representative assignments must be current

### Consistency
- Sales representative attributes must be consistent across all bookings
- Sales representative master data must reconcile with HR systems
- Sales team assignments must align with organizational structure

---

## Technical Implementation

### Source System
- **Schema**: quotetobooking
- **Table**: dim_sales_rep
- **Primary Key**: sales_rep_key (surrogate key)
- **Business Key**: rep_id
- **Type**: Slowly Changing Dimension (Type 2 recommended for tracking role/team changes)

### Key Attributes
- Sales Representative Key (Primary Key)
- Sales Representative ID (Business Key)
- Sales Representative Name
- Sales Role
- Sales Team
- Segment Covered

---

## Semantic Links

### Related Domains
- [Sales Transactions](sales-transactions.md)
- [Customer Management](customer-management.md)
- [Geography](geography.md)
- [Contract Management](contract-management.md)

### Related Glossary Terms
- [Sales Representative Dimension](../glossary/sales-representative-dimension.md)
- [Sales Representative Key](../glossary/sales-representative-key.md)
- [Sales Representative ID](../glossary/sales-representative-id.md)
- [Sales Representative Name](../glossary/sales-representative-name.md)
- [Sales Role](../glossary/sales-role.md)
- [Sales Team](../glossary/sales-team.md)
- [Segment Covered](../glossary/segment-covered.md)

---

## Navigation

- [Back to Domains Index](index.md)
- [Back to Bundle Index](../index.md)
