# Table Information

| Field | Value |
| --- | --- |
| Database Name | PostgreSQL |
| Table Name | QuoteToBooking.dim_product |

# Column Summary

| Column Name | Data Type | Nullable | Distinct Count | Null Count | Null % | Min | Max | Average |
| --- | --- | --- | ---: | ---: | ---: | --- | --- | --- |
| product_key | integer | NO | 10 | 0 | 0.00 | 1 | 9 | 5.50 |
| product_id | character varying | NO | 10 | 0 | 0.00 | C9300-48P | WBX-SUITE |  |
| product_name | character varying | YES | 10 | 0 | 0.00 | Catalyst 9300 Switch | Webex Suite |  |
| product_family | character varying | YES | 7 | 0 | 0.00 | Catalyst | Webex |  |
| technology_domain | character varying | YES | 7 | 0 | 0.00 | Collaboration | Security - Zero Trust |  |
| offer_type | character varying | YES | 3 | 0 | 0.00 | Hardware | Software Subscription |  |
| business_entity | character varying | YES | 5 | 0 | 0.00 | Collaboration | Security |  |

# Value Distribution Summary

## business_entity

| Value | Frequency |
| --- | ---: |
| Security | 4 |
| Meraki | 2 |
| Networking | 2 |
| Collaboration | 1 |
| Data Center | 1 |

## offer_type

| Value | Frequency |
| --- | ---: |
| Hardware | 5 |
| SaaS Subscription | 4 |
| Software Subscription | 1 |

## product_family

| Value | Frequency |
| --- | ---: |
| Catalyst | 2 |
| Firepower | 2 |
| Meraki | 2 |
| Duo | 1 |
| Nexus | 1 |
| Umbrella | 1 |
| Webex | 1 |

## technology_domain

| Value | Frequency |
| --- | ---: |
| Networking - Cloud Managed | 2 |
| Networking - Switching | 2 |
| Security - Network | 2 |
| Collaboration | 1 |
| Networking - Data Center | 1 |
| Security - SSE | 1 |
| Security - Zero Trust | 1 |

# Date Statistics

No date/timestamp columns.

# Text Statistics

| Column Name | Min Length | Max Length | Average Length |
| --- | ---: | ---: | ---: |
| product_id | 8 | 11 | 9.40 |
| product_name | 10 | 32 | 20.50 |
| product_family | 3 | 9 | 6.70 |
| technology_domain | 13 | 26 | 20.40 |
| offer_type | 8 | 21 | 12.90 |
| business_entity | 6 | 13 | 8.80 |
