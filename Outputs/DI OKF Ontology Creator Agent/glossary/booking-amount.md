---
title: Booking Amount
type: glossary
description: The total booked sales amount after pricing and discount adjustments
resource: glossary
tags: [booking-amount, revenue, sales]
timestamp: 2026-07-28T00:00:00Z
---

# Booking Amount

## Business Definition

Booking Amount is the total booked sales amount in US dollars after pricing and discount adjustments. It represents the net revenue value of a booking transaction, calculated by applying discounts to the list price multiplied by quantity.

---

## Business Meaning

Booking Amount is the primary revenue metric for sales transactions. It represents:
- The actual revenue value committed by the customer
- Net amount after all pricing adjustments and discounts
- The basis for revenue recognition and reporting
- The foundation for sales performance measurement

The booking amount reflects the final negotiated price and is the amount that will be invoiced to the customer.

---

## Technical Mapping

**Source Entity**: [Bookings](../entities/bookings.md)

**Source Field**: booking_amount_usd

**Calculation**: quantity × unit_list_price_usd × (1 - discount_pct)

---

## Synonyms

- Booked Revenue
- Sales Amount
- Transaction Amount
- Net Booking Value
- Booking Revenue

---

## Related Concepts

- [Booking Transaction](./booking-transaction.md) - Transaction containing booking amount
- [Discount Percentage](./discount-percentage.md) - Discount applied to calculate booking amount
- [Annual Contract Value](./annual-contract-value.md) - Annualized booking amount
- [Total Contract Value](./total-contract-value.md) - Total amount over contract term

---

## Related Entities

- [Bookings](../entities/bookings.md) - Contains booking amount values

---

## Related Measures

- [Total Booking Amount USD](../measures/total-booking-amount-usd.md) - Sum of all booking amounts
- [Renewal Booking Amount USD](../measures/renewal-booking-amount-usd.md) - Renewal portion
- [Net New Booking Amount USD](../measures/net-new-booking-amount-usd.md) - Net new portion
- [Average Booking Value USD](../measures/average-booking-value-usd.md) - Average per transaction

---

## Usage Context

Booking Amount is used for:
- Revenue tracking and reporting
- Sales performance measurement
- Quota attainment calculation
- Commission calculations
- Financial forecasting
- Deal size analysis
- Pricing effectiveness evaluation

---

## Business Rules

1. Booking amount must be non-negative
2. Booking amount is expressed in US dollars
3. Booking amount = quantity × unit_list_price_usd × (1 - discount_pct)
4. Booking amount represents net revenue after discounts
5. Booking amount is the basis for revenue recognition

---

## Calculation Example

**Example 1: No Discount**
- Quantity: 10 units
- Unit List Price: $1,000
- Discount: 0% (0.00)
- Booking Amount: 10 × $1,000 × (1 - 0.00) = $10,000

**Example 2: With Discount**
- Quantity: 10 units
- Unit List Price: $1,000
- Discount: 15% (0.15)
- Booking Amount: 10 × $1,000 × (1 - 0.15) = $8,500

---

## Related Domain

[Sales Bookings and Revenue Analytics](../domains/sales-bookings-and-revenue-analytics.md)
