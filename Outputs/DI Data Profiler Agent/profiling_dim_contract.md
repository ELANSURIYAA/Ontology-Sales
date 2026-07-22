# Table Information

| Field | Value |
| --- | --- |
| Database Name | PostgreSQL |
| Table Name | QuoteToBooking.dim_contract |

# Column Summary

| Column Name | Data Type | Nullable | Distinct Count | Null Count | Null % | Min | Max | Average |
| --- | --- | --- | ---: | ---: | ---: | --- | --- | --- |
| contract_key | integer | NO | 6 | 0 | 0.00 | 1 | 6 | 3.50 |
| contract_type | character varying | YES | 6 | 0 | 0.00 | Enterprise Agreement | Success Track L2 |  |
| term_months | integer | YES | 3 | 0 | 0.00 | 0 | 36 | 18.00 |
| auto_renew_flag | character | YES | 2 | 0 | 0.00 | N | Y |  |
| coverage_level | character varying | YES | 6 | 0 | 0.00 | 24x7 | Standard |  |

# Value Distribution Summary

## auto_renew_flag

| Value | Frequency |
| --- | ---: |
| Y | 4 |
| N | 2 |

## contract_type

| Value | Frequency |
| --- | ---: |
| Enterprise Agreement | 1 |
| Perpetual (no support) | 1 |
| SaaS Subscription | 1 |
| SmartNet Total Care | 1 |
| Solution Support | 1 |
| Success Track L2 | 1 |

## coverage_level

| Value | Frequency |
| --- | ---: |
| 24x7 | 1 |
| 24x7x4 | 1 |
| EA | 1 |
| Expert | 1 |
| None | 1 |
| Standard | 1 |

# Date Statistics

No date/timestamp columns.

# Text Statistics

| Column Name | Min Length | Max Length | Average Length |
| --- | ---: | ---: | ---: |
| contract_type | 16 | 22 | 18.33 |
| auto_renew_flag | 1 | 1 | 1.00 |
| coverage_level | 2 | 8 | 5.00 |
