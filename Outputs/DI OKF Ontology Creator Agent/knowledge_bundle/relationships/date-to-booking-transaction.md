---
title: Date to Booking Transaction
type: relationship
id: REL003
source_entity: Date
target_entity: Booking Transaction
relationship_type: Referential
cardinality: One-to-Many
version: 1.0
status: generated
---

# Date to Booking Transaction

## Source Entity

- [Date](../entities/date.md)

## Target Entity

- [Booking Transaction](../entities/booking-transaction.md)

## Relationship Type

Referential

## Cardinality

One-to-Many

## Business Description

A date can be associated with many booking transactions. Each booking transaction may reference a date through the foreign key `date_key`, enabling reporting across calendar periods and fiscal periods.