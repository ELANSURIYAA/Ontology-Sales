---
title: Product to Booking Transaction
type: relationship
id: REL006
source_entity: Product
target_entity: Booking Transaction
relationship_type: Referential
cardinality: One-to-Many
version: 1.0
status: generated
---

# Product to Booking Transaction

## Source Entity

- [Product](../entities/product.md)

## Target Entity

- [Booking Transaction](../entities/booking-transaction.md)

## Relationship Type

Referential

## Cardinality

One-to-Many

## Business Description

A product can be associated with many booking transactions. Each booking transaction may reference a product through the foreign key `product_key`, enabling analysis by product family, technology domain, offer type, and business entity.