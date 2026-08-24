---
title: Sales Order
type: glossary
description: A sales order containing one or more booking line items
resource: glossary
tags: [sales-order, order, transaction]
timestamp: 2026-07-28T00:00:00Z
---

# Sales Order

## Business Definition

A Sales Order is a commercial document that contains one or more booking line items representing products or services sold to a customer. Each sales order is identified by a unique order number and may contain multiple line items for different products, quantities, or pricing.

---

## Business Meaning

Sales Orders serve as:
- The container for booking transactions
- The primary reference for order fulfillment
- The basis for invoicing and billing
- The link between quote and booking
- The tracking mechanism for order processing

A single sales order can contain:
- Multiple products or services
- Different quantities and pricing per line
- Mixed product families or categories
- Various contract terms per line item

---

## Technical Mapping

**Source Entity**: [Bookings](../entities/bookings.md)

**Source Field**: order_number

**Relationship**: One order can have many booking line items

---

## Synonyms

- Order
- Purchase Order
- Sales Transaction
- Order Number
- Order Reference

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Individual line items within an order
- [Booking Amount](./booking-amount.md) - Revenue value of order lines

---

## Related Entities

- [Bookings](../entities/bookings.md) - Contains order_number and order_line_number

---

## Related Measures

- [Distinct Order Count](../measures/distinct-order-count.md) - Count of unique sales orders
- [Booking Count](../measures/booking-count.md) - Count of booking line items
- [Total Booking Amount USD](../measures/total-booking-amount-usd.md) - Total order value

---

## Usage Context

Sales Orders are used for:
- Order processing and fulfillment
- Invoicing and billing
- Revenue tracking
- Customer service and support
- Order status tracking
- Shipment coordination

---

## Business Rules

1. Each sales order has a unique order_number
2. A sales order can contain one or more booking line items
3. Each line item has a unique order_line_number within the order
4. All line items in an order reference the same order_number
5. Order-level attributes (customer, date) are consistent across all line items

---

## Order Structure

**Order Level:**
- order_number (unique identifier)
- Customer
- Order date
- Sales representative
- Partner

**Line Level (Booking Transactions):**
- order_line_number
- Product
- Quantity
- Pricing
- Discount
- Contract terms

---

## Derived Metrics

### Average Lines per Order
```
Booking Count / Distinct Order Count
```

### Average Order Value
```
Total Booking Amount USD / Distinct Order Count
```

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
