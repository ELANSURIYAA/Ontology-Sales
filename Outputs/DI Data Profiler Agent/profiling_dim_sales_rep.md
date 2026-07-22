# Table Information

| Field | Value |
| --- | --- |
| Database Name | PostgreSQL |
| Table Name | QuoteToBooking.dim_sales_rep |

# Column Summary

| Column Name | Data Type | Nullable | Distinct Count | Null Count | Null % | Min | Max | Average |
| --- | --- | --- | ---: | ---: | ---: | --- | --- | --- |
| sales_rep_key | integer | NO | 6 | 0 | 0.00 | 1 | 6 | 3.50 |
| rep_id | character varying | NO | 6 | 0 | 0.00 | REP-01 | REP-06 |  |
| rep_name | character varying | YES | 6 | 0 | 0.00 | Aisha Rahman | Robert Klein |  |
| sales_role | character varying | YES | 3 | 0 | 0.00 | Account Executive | Public Sector Account Manager |  |
| sales_team | character varying | YES | 6 | 0 | 0.00 | APJC SP | SP West |  |
| segment_covered | character varying | YES | 3 | 0 | 0.00 | Enterprise | Service Provider |  |

# Value Distribution Summary

## sales_role

| Value | Frequency |
| --- | ---: |
| Account Executive | 4 |
| Enterprise Account Manager | 1 |
| Public Sector Account Manager | 1 |

## sales_team

| Value | Frequency |
| --- | ---: |
| APJC SP | 1 |
| EMEA SP | 1 |
| Enterprise FSI | 1 |
| Federal | 1 |
| SP East | 1 |
| SP West | 1 |

## segment_covered

| Value | Frequency |
| --- | ---: |
| Service Provider | 4 |
| Enterprise | 1 |
| Public Sector | 1 |

# Date Statistics

No date/timestamp columns.

# Text Statistics

| Column Name | Min Length | Max Length | Average Length |
| --- | ---: | ---: | ---: |
| rep_id | 6 | 6 | 6.00 |
| rep_name | 10 | 14 | 12.00 |
| sales_role | 17 | 29 | 20.50 |
| sales_team | 7 | 14 | 8.17 |
| segment_covered | 10 | 16 | 14.50 |
