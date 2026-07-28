---
title: Sales Representative ID
type: glossary
description: Business identifier assigned to the sales representative
resource: glossary
tags: [glossary, sales-rep, identifier, business-key]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Representative ID

## Business Definition

Business identifier assigned to the sales representative.

---

## Business Meaning

Sales Representative ID is the business-level identifier used to reference sales personnel in operational systems, HR systems, and business communications. Unlike the surrogate Sales Representative Key, the Sales Representative ID is a meaningful business identifier used in employee management and sales operations.

---

## Technical Mapping

**Source Schema**: QuoteToBooking  
**Source Table**: dim_sales_rep  
**Source Column**: rep_id  
**Entity**: [Sales Representative](../entities/sales-representative.md)  
**Attribute**: Sales Representative ID  
**Data Type**: character varying(20)  
**Nullable**: No  
**Confidence Score**: 1.00

---

## Synonyms

- Rep ID
- Employee ID
- Sales Rep Number

---

## Related Concepts

### Related Entities
- [Sales Representative](../entities/sales-representative.md)

### Related Attributes
- [Sales Representative Key](sales-representative-key.md)
- [Sales Representative Name](sales-representative-name.md)

---

## Usage Context

Sales Representative ID is used to:
- Identify sales personnel in business operations
- Link to HR and employee systems
- Support sales performance tracking

---

## Navigation

- [View Glossary Index](index.md)
- [View Sales Representative Entity](../entities/sales-representative.md)
- [Return to Bundle Index](../index.md)

---

## Metadata

**Term Type**: Attribute  
**Source Entity**: Sales Representative  
**Source Attribute**: Sales Representative ID  
**Confidence Score**: 1.00  
**Last Updated**: 2026-07-28T00:00:00Z
