---
title: Contract to Booking Transaction
type: relationship
id: REL001
source_entity: Contract
target_entity: Booking Transaction
relationship_type: Referential
cardinality: One-to-Many
version: 1.0
status: generated
---

# Contract to Booking Transaction

## Source Entity

- [Contract](../entities/contract.md)

## Target Entity

- [Booking Transaction](../entities/booking-transaction.md)

## Relationship Type

Referential

## Cardinality

One-to-Many

## Business Description

A contract can be associated with many booking transactions. Each booking transaction may reference a contract through the foreign key `contract_key`, enabling analysis of bookings by contract type, duration, renewal behavior, and coverage level.