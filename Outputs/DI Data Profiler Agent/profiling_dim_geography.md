# Table Information

| Field | Value |
| --- | --- |
| Database Name | PostgreSQL |
| Table Name | QuoteToBooking.dim_geography |

# Column Summary

| Column Name | Data Type | Nullable | Distinct Count | Null Count | Null % | Min | Max | Average |
| --- | --- | --- | ---: | ---: | ---: | --- | --- | --- |
| geography_key | integer | NO | 8 | 0 | 0.00 | 1 | 8 | 4.50 |
| region | character varying | YES | 3 | 0 | 0.00 | Americas | EMEA |  |
| theater | character varying | YES | 8 | 0 | 0.00 | ANZ | US Commercial |  |
| country | character varying | YES | 8 | 0 | 0.00 | Australia | United States |  |

# Value Distribution Summary

## country

| Value | Frequency |
| --- | ---: |
| Australia | 1 |
| Canada | 1 |
| Germany | 1 |
| India | 1 |
| Japan | 1 |
| United Arab Emirates | 1 |
| United Kingdom | 1 |
| United States | 1 |

## region

| Value | Frequency |
| --- | ---: |
| APJC | 3 |
| EMEA | 3 |
| Americas | 2 |

## theater

| Value | Frequency |
| --- | ---: |
| ANZ | 1 |
| Canada | 1 |
| Central Europe | 1 |
| India | 1 |
| Japan | 1 |
| Middle East | 1 |
| Northern Europe | 1 |
| US Commercial | 1 |

# Date Statistics

No date/timestamp columns.

# Text Statistics

| Column Name | Min Length | Max Length | Average Length |
| --- | ---: | ---: | ---: |
| region | 4 | 8 | 5.00 |
| theater | 3 | 15 | 9.00 |
| country | 5 | 20 | 9.88 |
