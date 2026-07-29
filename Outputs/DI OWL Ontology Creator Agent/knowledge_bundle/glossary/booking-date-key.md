---
title: Booking Date Key
type: glossary
description: Foreign key linking the booking transaction to the reporting date dimension
resource: glossary
tags: [booking, transaction, date, foreign-key, attribute]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Date Key

## Business Definition

Foreign key linking the booking transaction to the reporting date dimension.

---

## Business Meaning

Booking Date Key is the foreign key that links each booking transaction to its corresponding date in the date dimension, enabling temporal analysis of booking transactions.

---

## Technical Mapping

**Source System:** QuoteToBooking  
**Source Table:** fact_bookings  
**Source Column:** date_key  
**Data Type:** Integer  
**Entity:** [Booking Transaction](../entities/booking-transaction.md)  
**Attribute:** Booking Date Key  
**Confidence Score:** 1.00

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Parent entity
- [Date](./date.md) - Referenced dimension
- [Date Key](./date-key.md) - Primary key in date dimension

---

## Usage Context

Booking Date Key is used to:
- Link transactions to date attributes
- Enable temporal analysis
- Support time-based filtering and grouping
- Provide referential integrity to date dimension

---

## Navigation

- [Return to Glossary Index](./index.md)
- [View Entity Definition](../entities/booking-transaction.md)
- [Return to Bundle Index](../index.md)
