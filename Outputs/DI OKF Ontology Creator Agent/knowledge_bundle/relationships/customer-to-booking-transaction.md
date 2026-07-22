---
title: Customer to Booking Transaction
type: relationship
id: REL002
source_entity: Customer
target_entity: Booking Transaction
relationship_type: Referential
cardinality: One-to-Many
version: 1.0
status: generated
---

# Customer to Booking Transaction

## Source Entity

- [Customer](../entities/customer.md)

## Target Entity

- [Booking Transaction](../entities/booking-transaction.md)

## Relationship Type

Referential

## Cardinality

One-to-Many

## Business Description

A customer can be associated with many booking transactions. Each booking transaction may reference a customer through the foreign key `customer_key`, enabling analysis by customer identity, segment, industry, account tier, and headquarters geography.