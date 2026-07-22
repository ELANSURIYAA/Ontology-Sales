---
title: Sales Representative to Booking Transaction
type: relationship
id: REL007
source_entity: Sales Representative
target_entity: Booking Transaction
relationship_type: Referential
cardinality: One-to-Many
version: 1.0
status: generated
---

# Sales Representative to Booking Transaction

## Source Entity

- [Sales Representative](../entities/sales-representative.md)

## Target Entity

- [Booking Transaction](../entities/booking-transaction.md)

## Relationship Type

Referential

## Cardinality

One-to-Many

## Business Description

A sales representative can be associated with many booking transactions. Each booking transaction may reference a sales representative through the foreign key `sales_rep_key`, enabling analysis of seller performance by role, team, and covered segment.