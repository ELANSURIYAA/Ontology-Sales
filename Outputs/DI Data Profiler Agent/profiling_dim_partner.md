# Table Information

| Field | Value |
| --- | --- |
| Database Name | PostgreSQL |
| Table Name | QuoteToBooking.dim_partner |

# Column Summary

| Column Name | Data Type | Nullable | Distinct Count | Null Count | Null % | Min | Max | Average |
| --- | --- | --- | ---: | ---: | ---: | --- | --- | --- |
| partner_key | integer | NO | 6 | 0 | 0.00 | 1 | 6 | 3.50 |
| partner_id | character varying | NO | 6 | 0 | 0.00 | PTR-01 | PTR-06 |  |
| partner_name | character varying | YES | 6 | 0 | 0.00 | CDW | World Wide Technology |  |
| partner_type | character varying | YES | 4 | 0 | 0.00 | Direct | Value-Added Reseller |  |
| partner_tier | character varying | YES | 5 | 0 | 0.00 | Authorized Distributor | Select |  |
| route_to_market | character varying | YES | 3 | 0 | 0.00 | Direct | Two-Tier |  |

# Value Distribution Summary

## partner_tier

| Value | Frequency |
| --- | ---: |
| Gold Integrator | 2 |
| Authorized Distributor | 1 |
| N/A | 1 |
| Premier | 1 |
| Select | 1 |

## partner_type

| Value | Frequency |
| --- | ---: |
| Value-Added Reseller | 3 |
| Direct | 1 |
| Distributor | 1 |
| Systems Integrator | 1 |

## route_to_market

| Value | Frequency |
| --- | ---: |
| Reseller | 3 |
| Two-Tier | 2 |
| Direct | 1 |

# Date Statistics

No date/timestamp columns.

# Text Statistics

| Column Name | Min Length | Max Length | Average Length |
| --- | ---: | ---: | ---: |
| partner_id | 6 | 6 | 6.00 |
| partner_name | 3 | 21 | 10.67 |
| partner_type | 6 | 20 | 15.83 |
| partner_tier | 3 | 22 | 11.33 |
| route_to_market | 6 | 8 | 7.67 |
