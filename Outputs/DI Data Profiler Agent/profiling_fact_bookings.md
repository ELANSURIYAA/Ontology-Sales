# Table Information

| Field | Value |
| --- | --- |
| Database Name | ontology |
| Table Name | quotetobooking.fact_bookings |

# Column Summary

| Column Name | Data Type | Nullable | Distinct Count | Null Count | Null % | Min | Max | Average |
| --- | --- | --- | ---: | ---: | ---: | --- | --- | --- |
| booking_id | integer | NO | 10 | 0 | 0.00 | 1 | 10 | 5.5000000000000000 |
| order_number | character varying | YES | 10 | 0 | 0.00 | ORD-5001 | ORD-5010 |  |
| order_line_number | integer | YES | 1 | 0 | 0.00 | 1 | 1 | 1.00000000000000000000 |
| date_key | integer | YES | 7 | 0 | 0.00 | 20241215 | 20260615 | 20250795.000000000000 |
| customer_key | integer | YES | 2 | 0 | 0.00 | 1 | 2 | 1.3000000000000000 |
| product_key | integer | YES | 5 | 0 | 0.00 | 1 | 10 | 3.6000000000000000 |
| partner_key | integer | YES | 3 | 0 | 0.00 | 1 | 4 | 1.6000000000000000 |
| geography_key | integer | YES | 1 | 0 | 0.00 | 1 | 1 | 1.00000000000000000000 |
| sales_rep_key | integer | YES | 2 | 0 | 0.00 | 1 | 2 | 1.3000000000000000 |
| contract_key | integer | YES | 2 | 0 | 0.00 | 1 | 5 | 2.2000000000000000 |
| booking_type | character varying | YES | 2 | 0 | 0.00 | New | Renewal |  |
| is_renewal | integer | YES | 2 | 0 | 0.00 | 0 | 1 | 0.40000000000000000000 |
| quantity | integer | YES | 7 | 0 | 0.00 | 4 | 250 | 98.2000000000000000 |
| unit_list_price_usd | numeric | YES | 5 | 0 | 0.00 | 8000.00 | 50000.00 | 22400.000000000000 |
| discount_pct | numeric | YES | 7 | 0 | 0.00 | 0.11 | 0.28 | 0.17800000000000000000 |
| booking_amount_usd | numeric | YES | 10 | 0 | 0.00 | 130000.00 | 2670000.00 | 900500.000000000000 |
| acv_usd | numeric | YES | 10 | 0 | 0.00 | 43333.00 | 2670000.00 | 545700.000000000000 |
| tcv_usd | numeric | YES | 10 | 0 | 0.00 | 130000.00 | 2670000.00 | 900500.000000000000 |

# Value Distribution Summary

## booking_type

| Value | Frequency |
| --- | ---: |
| New | 6 |
| Renewal | 4 |

## is_renewal

| Value | Frequency |
| --- | ---: |
| 0 | 6 |
| 1 | 4 |

# Date Statistics

| Column Name | Min Date | Max Date | Distinct Count |
| --- | --- | --- | ---: |

# Text Statistics

| Column Name | Min Length | Max Length | Average Length |
| --- | ---: | ---: | ---: |
| order_number | 8 | 8 | 8.00 |
| booking_type | 3 | 7 | 4.60 |
