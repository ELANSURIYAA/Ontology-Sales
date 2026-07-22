---
title: Partner to Booking Transaction
type: relationship
id: REL005
source_entity: Partner
target_entity: Booking Transaction
relationship_type: Referential
cardinality: One-to-Many
version: 1.0
status: generated
---

# Partner to Booking Transaction

## Source Entity

- [Partner](../entities/partner.md)

## Target Entity

- [Booking Transaction](../entities/booking-transaction.md)

## Relationship Type

Referential

## Cardinality

One-to-Many

## Business Description

A partner can be associated with many booking transactions. Each booking transaction may reference a partner through the foreign key `partner_key`, enabling analysis of direct and indirect channel performance.