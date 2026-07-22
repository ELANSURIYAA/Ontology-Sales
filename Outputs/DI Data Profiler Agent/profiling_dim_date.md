# Table Information

| Field | Value |
| --- | --- |
| Database Name | PostgreSQL |
| Table Name | QuoteToBooking.dim_date |

# Column Summary

| Column Name | Data Type | Nullable | Distinct Count | Null Count | Null % | Min | Max | Average |
| --- | --- | --- | ---: | ---: | ---: | --- | --- | --- |
| date_key | integer | NO | 12 | 0 | 0.00 | 20230915 | 20260615 | 20245765.00 |
| full_date | date | NO | 12 | 0 | 0.00 | 2023-09-15 | 2026-06-15 |  |
| month_name | character varying | YES | 4 | 0 | 0.00 | December | September |  |
| calendar_year | integer | YES | 4 | 0 | 0.00 | 2023 | 2026 | 2024.50 |
| fiscal_year | character varying | YES | 3 | 0 | 0.00 | FY24 | FY26 |  |
| fiscal_quarter | character varying | YES | 12 | 0 | 0.00 | FY24 Q1 | FY26 Q4 |  |
| fiscal_period_seq | integer | YES | 12 | 0 | 0.00 | 1 | 9 | 6.50 |

# Value Distribution Summary

## calendar_year

| Value | Frequency |
| --- | ---: |
| 2024 | 4 |
| 2025 | 4 |
| 2023 | 2 |
| 2026 | 2 |

## fiscal_quarter

| Value | Frequency |
| --- | ---: |
| FY24 Q1 | 1 |
| FY24 Q2 | 1 |
| FY24 Q3 | 1 |
| FY24 Q4 | 1 |
| FY25 Q1 | 1 |
| FY25 Q2 | 1 |
| FY25 Q3 | 1 |
| FY25 Q4 | 1 |
| FY26 Q1 | 1 |
| FY26 Q2 | 1 |
| FY26 Q3 | 1 |
| FY26 Q4 | 1 |

## fiscal_year

| Value | Frequency |
| --- | ---: |
| FY24 | 4 |
| FY25 | 4 |
| FY26 | 4 |

## month_name

| Value | Frequency |
| --- | ---: |
| December | 3 |
| June | 3 |
| March | 3 |
| September | 3 |

# Date Statistics

| Column Name | Min Date | Max Date | Distinct Count |
| --- | --- | --- | ---: |
| full_date | 2023-09-15 | 2026-06-15 | 12 |

# Text Statistics

| Column Name | Min Length | Max Length | Average Length |
| --- | ---: | ---: | ---: |
| month_name | 4 | 9 | 6.50 |
| fiscal_year | 4 | 4 | 4.00 |
| fiscal_quarter | 7 | 7 | 7.00 |
