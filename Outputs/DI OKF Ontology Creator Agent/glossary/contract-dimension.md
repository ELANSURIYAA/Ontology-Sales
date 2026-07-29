---
title: Contract Dimension
type: glossary
description: Stores contract and service agreement attributes used to classify bookings
resource: glossary
tags: [okf, glossary, entity, contract, dimension]
timestamp: 2026-07-28T00:00:00Z
---

# Contract Dimension

## Business Definition

Stores contract and service agreement attributes used to classify bookings by contract type, term, renewal behavior, and coverage level.

---

## Technical Mapping

**Source Table**: quotetobooking.dim_contract  
**Entity**: Contract Dimension  
**Attribute**: N/A (Entity-level term)

---

## Business Meaning

The Contract Dimension provides contractual context for booking transactions. It enables analysis of bookings by contract characteristics such as agreement type, contract duration, auto-renewal settings, and service coverage levels. This dimension supports contract lifecycle management and renewal forecasting.

---

## Related Concepts

- [Contract Key](contract-key.md)
- [Contract Type](contract-type.md)
- [Contract Term Months](contract-term-months.md)
- [Auto Renew Flag](auto-renew-flag.md)
- [Coverage Level](coverage-level.md)
- [Booking Fact](booking-fact.md)

---

## Navigation

- [Back to Glossary Index](index.md)
- [Back to Bundle Index](../index.md)
