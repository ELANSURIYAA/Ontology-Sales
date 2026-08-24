# Table Information

| Field | Value |
| --- | --- |
| Database Name | ontology |
| Table Name | clarity.client |

# Column Summary

| Column Name | Data Type | Nullable | Distinct Count | Null Count | Null % | Min | Max | Average |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| client_id | bigint | YES | 10 | 0 | 0.00 | 10001 | 10010 | 10005.50 |
| migration_date | date | YES | 10 | 0 | 0.00 | 2026-01-15 | 2026-08-01 |  |
| financial_institution_name | character varying | YES | 10 | 0 | 0.00 | Atlantic Trust Bank | United Regional Bank |  |
| entity_id | bigint | YES | 10 | 0 | 0.00 | 501 | 510 | 505.50 |
| cardcount | integer | YES | 10 | 0 | 0.00 | 5600 | 22100 | 12100.00 |
| vru_activation_options | character varying | YES | 6 | 0 | 0.00 | IVR | SMS, Mobile App |  |
| fi_id | bigint | YES | 10 | 0 | 0.00 | 2001 | 2010 | 2005.50 |
| aims_id | bigint | YES | 10 | 0 | 0.00 | 3001 | 3010 | 3005.50 |
| ig_league_name | character varying | YES | 4 | 0 | 0.00 | League-A | League-D |  |
| arb | numeric | YES | 10 | 0 | 0.00 | 540000.10 | 4100000.95 | 1621500.42 |
| routing_id | character varying | YES | 10 | 0 | 0.00 | 111000025 | 999000011 |  |
| city | character varying | YES | 10 | 0 | 0.00 | Atlanta | Seattle |  |
| state_name | character varying | YES | 10 | 0 | 0.00 | California | Washington |  |
| fi_primary_contact_name | character varying | YES | 10 | 0 | 0.00 | David Anderson | Sarah Johnson |  |
| fi_primary_contact_phone | character varying | YES | 10 | 0 | 0.00 | +1-206-555-1010 | +1-617-555-1005 |  |
| fraudcontactgroup_email | character varying | YES | 10 | 0 | 0.00 | fraud@atlantictrust.com | fraud@unitedregional.com |  |
| address | character varying | YES | 10 | 0 | 0.00 | 1000 Pike Street | 900 Woodward Avenue |  |
| zip | character varying | YES | 10 | 0 | 0.00 | 02110 | 98101 |  |
| fi_primary_contact_email | character varying | YES | 10 | 0 | 0.00 | david.anderson@mountainstate.com | sarah.johnson@communitycu.com |  |
| current_pseudorouting | character varying | YES | 10 | 0 | 0.00 | PR10001 | PR10010 |  |
| issuing_networks | character varying | YES | 6 | 0 | 0.00 | MASTERCARD | VISA, MASTERCARD, AMEX |  |
| aquiring_networks | character varying | YES | 4 | 0 | 0.00 | MASTERCARD | VISA, MASTERCARD |  |
| vau_segment_id | bigint | YES | 10 | 0 | 0.00 | 101 | 110 | 105.50 |
| migration_wave | integer | YES | 5 | 0 | 0.00 | 1 | 5 | 3.00 |

# Value Distribution Summary

## financial_institution_name

| Value | Frequency |
| --- | --- |
| Atlantic Trust Bank | 1 |
| Community Credit Union | 1 |
| First National Bank | 1 |
| Great Lakes Credit Union | 1 |
| Metro Bank | 1 |
| Mountain State Bank | 1 |
| National Commerce Bank | 1 |
| Pacific Financial Services | 1 |
| Sunrise Financial | 1 |
| United Regional Bank | 1 |

## vru_activation_options

| Value | Frequency |
| --- | --- |
| IVR | 2 |
| IVR, SMS | 2 |
| IVR, SMS, Mobile App | 2 |
| SMS, Mobile App | 2 |
| IVR, Mobile App | 1 |
| SMS | 1 |

## ig_league_name

| Value | Frequency |
| --- | --- |
| League-A | 4 |
| League-B | 2 |
| League-C | 2 |
| League-D | 2 |

## city

| Value | Frequency |
| --- | --- |
| Atlanta | 1 |
| Boston | 1 |
| Chicago | 1 |
| Dallas | 1 |
| Denver | 1 |
| Detroit | 1 |
| Miami | 1 |
| New York | 1 |
| San Francisco | 1 |
| Seattle | 1 |

## state_name

| Value | Frequency |
| --- | --- |
| California | 1 |
| Colorado | 1 |
| Florida | 1 |
| Georgia | 1 |
| Illinois | 1 |
| Massachusetts | 1 |
| Michigan | 1 |
| New York | 1 |
| Texas | 1 |
| Washington | 1 |

## issuing_networks

| Value | Frequency |
| --- | --- |
| MASTERCARD | 2 |
| VISA | 2 |
| VISA, MASTERCARD | 2 |
| VISA, MASTERCARD, AMEX | 2 |
| MASTERCARD, VISA | 1 |
| VISA, AMEX | 1 |

## aquiring_networks

| Value | Frequency |
| --- | --- |
| MASTERCARD | 4 |
| VISA | 3 |
| VISA, MASTERCARD | 2 |
| VISA, AMEX | 1 |

# Date Statistics

| Column Name | Min Date | Max Date | Distinct Count |
| --- | --- | --- | --- |
| migration_date | 2026-01-15 | 2026-08-01 | 10 |

# Text Statistics

| Column Name | Min Length | Max Length | Average Length |
| --- | --- | --- | --- |
| financial_institution_name | 10 | 26 | 19.80 |
| vru_activation_options | 3 | 20 | 11.00 |
| ig_league_name | 8 | 8 | 8.00 |
| routing_id | 9 | 9 | 9.00 |
| city | 5 | 13 | 7.20 |
| state_name | 5 | 13 | 8.40 |
| fi_primary_contact_name | 10 | 15 | 12.70 |
| fi_primary_contact_phone | 15 | 15 | 15.00 |
| fraudcontactgroup_email | 19 | 26 | 23.30 |
| address | 15 | 20 | 17.10 |
| zip | 5 | 5 | 5.00 |
| fi_primary_contact_email | 25 | 36 | 31.00 |
| current_pseudorouting | 7 | 7 | 7.00 |
| issuing_networks | 4 | 22 | 13.00 |
| aquiring_networks | 4 | 16 | 9.40 |