---
title: Sales Representative Key
type: glossary
description: Surrogate key that uniquely identifies a sales representative record in the sales representative dimension
resource: glossary
tags: [glossary, sales-rep, key, identifier, surrogate-key]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative Key

## Business Definition

Surrogate key that uniquely identifies a sales representative record in the sales representative dimension.

---

## Business Meaning

Sales Representative Key is a system-generated unique identifier used to link sales representative records to booking transactions. It serves as the primary key for the sales representative dimension and enables efficient joins and referential integrity in the data model.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_sales_rep  
**Source Column**: sales_rep_key  
**Entity**: [Sales Representative](../entities/sales-representative.md)  
**Attribute**: Sales Representative Key  
**Data Type**: integer  
**Nullable**: No  
**Primary Key**: Yes  
**Confidence Score**: 1.00

---

## Synonyms

- Sales Rep Key
- Sales Representative Identifier
- Sales Rep Surrogate Key

---

## Related Concepts

### Related Entities
- [Sales Representative](../entities/sales-representative.md)
- [Booking Transaction](../entities/booking-transaction.md)

### Related Relationships
- [Sales Representative to Booking Transaction](../relationships/sales-representative-to-booking-transaction.md)

---

## Usage Context

Sales Representative Key is used to:
- Uniquely identify sales representative records
- Link booking transactions to sales representatives
- Enable dimensional analysis by sales representative attributes
- Maintain referential integrity

---

## Navigation

- [View Glossary Index](index.md)
- [View Sales Representative Entity](../entities/sales-representative.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Sales Representative  
**Source Attribute**: Sales Representative Key  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
