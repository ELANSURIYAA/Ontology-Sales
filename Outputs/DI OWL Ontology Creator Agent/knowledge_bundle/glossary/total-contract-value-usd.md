---
title: Total Contract Value USD
type: glossary
description: Total value of the full contract associated with the booking in U.S. dollars
resource: glossary
tags: [booking, transaction, contract, tcv, financial, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Total Contract Value USD

## Business Definition

Total value of the full contract associated with the booking in U.S. dollars.

---

## Business Meaning

Total Contract Value USD represents the complete value of a contract over its entire term, providing visibility into long-term revenue commitments. This metric is essential for understanding total customer commitment and contract portfolio value.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Source Column:** tcv_usd  
**Data Type:** Numeric  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Attribute:** Total Contract Value USD  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Parent entity
- [Annual Contract Value USD](./annual-contract-value-usd.md) - Annualized value
- [Booking Amount USD](./booking-amount-usd.md) - Initial booking revenue
- [Contract Term Months](./contract-term-months.md) - Contract duration

---

## Usage Context

Total Contract Value USD is used to:
- Track total committed revenue
- Analyze contract portfolio value
- Project long-term revenue
- Calculate customer lifetime value

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [View Measure Definition](../measures/total-contract-value-usd.md)
- [Return to Bundle Index](../index.md)
