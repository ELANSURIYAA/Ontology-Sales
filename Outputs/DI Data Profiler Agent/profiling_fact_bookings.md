# Table Information

| Field | Value |
| --- | --- |
| Database Name | PostgreSQL |
| Table Name | QuoteToBooking.fact_bookings |

# Column Summary

| Column Name | Data Type | Nullable | Distinct Count | Null Count | Null % | Min | Max | Average |
| --- | --- | --- | ---: | ---: | ---: | --- | --- | --- |
| booking_id | integer | NO | 10 | 0 | 0.00 | 1 | 9 | 5.50 |
| order_number | character varying | YES | 10 | 0 | 0.00 | ORD-5001 | ORD-5010 |  |
| order_line_number | integer | YES | 1 | 0 | 0.00 | 1 | 1 | 1.00 |
| date_key | integer | YES | 7 | 0 | 0.00 | 20241215 | 20260615 | 20250795.00 |
| customer_key | integer | YES | 2 | 0 | 0.00 | 1 | 2 | 1.30 |
| product_key | integer | YES | 5 | 0 | 0.00 | 1 | 7 | 3.60 |
| partner_key | integer | YES | 3 | 0 | 0.00 | 1 | 4 | 1.60 |
| geography_key | integer | YES | 1 | 0 | 0.00 | 1 | 1 | 1.00 |
| sales_rep_key | integer | YES | 2 | 0 | 0.00 | 1 | 2 | 1.30 |
| contract_key | integer | YES | 2 | 0 | 0.00 | 1 | 5 | 2.20 |
| booking_type | character varying | YES | 2 | 0 | 0.00 | New | Renewal |  |
| is_renewal | integer | YES | 2 | 0 | 0.00 | 0 | 1 | 0.40 |
| quantity | integer | YES | 7 | 0 | 0.00 | 10 | 8 | 98.20 |
| unit_list_price_usd | numeric | YES | 5 | 0 | 0.00 | 15000.00 | 8000.00 | 22400.00 |
| discount_pct | numeric | YES | 7 | 0 | 0.00 | 0.11 | 0.28 | 0.18 |
| booking_amount_usd | numeric | YES | 10 | 0 | 0.00 | 1008000.00 | 638000.00 | 900500.00 |
| acv_usd | numeric | YES | 10 | 0 | 0.00 | 118667.00 | 638000.00 | 545700.00 |
| tcv_usd | numeric | YES | 10 | 0 | 0.00 | 1008000.00 | 638000.00 | 900500.00 |

# Value Distribution Summary

## booking_type

| Value | Frequency |
| --- | ---: |
| New | 6 |
| Renewal | 4 |

## contract_key

| Value | Frequency |
| --- | ---: |
| 1 | 7 |
| 5 | 3 |

## customer_key

| Value | Frequency |
| --- | ---: |
| 1 | 7 |
| 2 | 3 |

## date_key

| Value | Frequency |
| --- | ---: |
| 20241215 | 2 |
| 20250315 | 2 |
| 20251215 | 2 |
| 20250615 | 1 |
| 20250915 | 1 |
| 20260315 | 1 |
| 20260615 | 1 |

## geography_key

| Value | Frequency |
| --- | ---: |
| 1 | 10 |

## is_renewal

| Value | Frequency |
| --- | ---: |
| 0 | 6 |
| 1 | 4 |

## order_line_number

| Value | Frequency |
| --- | ---: |
| 1 | 10 |

## partner_key

| Value | Frequency |
| --- | ---: |
| 1 | 6 |
| 2 | 3 |
| 4 | 1 |

## product_key

| Value | Frequency |
| --- | ---: |
| 1 | 4 |
| 3 | 2 |
| 7 | 2 |
| 10 | 1 |
| 2 | 1 |

## sales_rep_key

| Value | Frequency |
| --- | ---: |
| 1 | 7 |
| 2 | 3 |

# Date Statistics

No date/timestamp columns.

# Text Statistics

| Column Name | Min Length | Max Length | Average Length |
| --- | ---: | ---: | ---: |
| order_number | 8 | 8 | 8.00 |
| booking_type | 3 | 7 | 4.60 |
