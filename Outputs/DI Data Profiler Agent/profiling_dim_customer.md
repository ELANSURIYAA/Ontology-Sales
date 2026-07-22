# Table Information

| Field | Value |
| --- | --- |
| Database Name | PostgreSQL |
| Table Name | QuoteToBooking.dim_customer |

# Column Summary

| Column Name | Data Type | Nullable | Distinct Count | Null Count | Null % | Min | Max | Average |
| --- | --- | --- | ---: | ---: | ---: | --- | --- | --- |
| customer_key | integer | NO | 8 | 0 | 0.00 | 1 | 8 | 4.50 |
| customer_id | character varying | NO | 8 | 0 | 0.00 | CUST-1001 | CUST-1008 |  |
| customer_name | character varying | YES | 8 | 0 | 0.00 | AT&T | Vodafone |  |
| segment | character varying | YES | 3 | 0 | 0.00 | Enterprise | Service Provider |  |
| industry | character varying | YES | 3 | 0 | 0.00 | Financial Services | Telecommunications |  |
| account_tier | character varying | YES | 2 | 0 | 0.00 | Growth | Strategic |  |
| hq_country | character varying | YES | 5 | 0 | 0.00 | Germany | United States |  |
| hq_region | character varying | YES | 3 | 0 | 0.00 | Americas | EMEA |  |

# Value Distribution Summary

## account_tier

| Value | Frequency |
| --- | ---: |
| Growth | 4 |
| Strategic | 4 |

## hq_country

| Value | Frequency |
| --- | ---: |
| United States | 4 |
| Germany | 1 |
| India | 1 |
| Japan | 1 |
| United Kingdom | 1 |

## hq_region

| Value | Frequency |
| --- | ---: |
| Americas | 4 |
| APJC | 2 |
| EMEA | 2 |

## industry

| Value | Frequency |
| --- | ---: |
| Telecommunications | 6 |
| Financial Services | 1 |
| Government | 1 |

## segment

| Value | Frequency |
| --- | ---: |
| Service Provider | 6 |
| Enterprise | 1 |
| Public Sector | 1 |

# Date Statistics

No date/timestamp columns.

# Text Statistics

| Column Name | Min Length | Max Length | Average Length |
| --- | ---: | ---: | ---: |
| customer_id | 9 | 9 | 9.00 |
| customer_name | 3 | 26 | 11.25 |
| segment | 10 | 16 | 14.88 |
| industry | 10 | 18 | 17.00 |
| account_tier | 6 | 9 | 7.50 |
| hq_country | 5 | 14 | 10.38 |
| hq_region | 4 | 8 | 6.00 |
