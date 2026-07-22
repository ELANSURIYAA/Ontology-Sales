---
title: Geography to Booking Transaction
type: relationship
id: REL004
source_entity: Geography
target_entity: Booking Transaction
relationship_type: Referential
cardinality: One-to-Many
version: 1.0
status: generated
---

# Geography to Booking Transaction

## Source Entity

- [Geography](../entities/geography.md)

## Target Entity

- [Booking Transaction](../entities/booking-transaction.md)

## Relationship Type

Referential

## Cardinality

One-to-Many

## Business Description

A geography can be associated with many booking transactions. Each booking transaction may reference a geography through the foreign key `geography_key`, enabling analysis by region, theater, and country.