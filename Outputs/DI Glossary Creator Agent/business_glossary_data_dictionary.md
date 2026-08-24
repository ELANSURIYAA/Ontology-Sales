# Business Glossary Data Dictionary

## Business Domain Context
Business domain context file `Ontology-Sales/Inputs/Sales.txt` was not accessible from the repository at the provided path. The glossary below is therefore inferred from the supplied schema metadata, table relationships, and profiling results for the quote-to-booking sales domain.

# Table: quotetobooking.dim_contract

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_contract |
| Business Term | Contract Dimension |
| Business Definition | Stores descriptive contract attributes used to classify bookings by contract structure, duration, renewal behavior, and coverage level. |
| Business Category | Contracts |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| contract_key | Contract Key | Unique surrogate key for the contract record used to join contract details to booking transactions. | integer | Contracts |
| contract_type | Contract Type | Type of customer contract or service agreement associated with the booking. | character varying(40) | Contracts |
| term_months | Contract Term Months | Number of months covered by the contract term. | integer | Contracts |
| auto_renew_flag | Auto Renew Flag | Indicates whether the contract is set to renew automatically at the end of its term. | character(1) | Contracts |
| coverage_level | Coverage Level | Service or support coverage level provided under the contract. | character varying(20) | Contracts |

---

# Table: quotetobooking.dim_customer

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_customer |
| Business Term | Customer Dimension |
| Business Definition | Stores customer master data used to analyze bookings by customer identity, segment, industry, tier, and headquarters location. | 
| Business Category | Customers |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| customer_key | Customer Key | Unique surrogate key for the customer record used to join customer details to booking transactions. | integer | Customers |
| customer_id | Customer Identifier | Business identifier assigned to the customer account. | character varying(20) | Customers |
| customer_name | Customer Name | Name of the customer account or organization. | character varying(80) | Customers |
| segment | Customer Segment | Market segment to which the customer belongs, such as enterprise, service provider, or public sector. | character varying(30) | Customers |
| industry | Industry | Industry classification of the customer account. | character varying(40) | Customers |
| account_tier | Account Tier | Strategic classification of the customer account based on business importance or growth potential. | character varying(20) | Customers |
| hq_country | Headquarters Country | Country where the customer’s headquarters is located. | character varying(40) | Customers |
| hq_region | Headquarters Region | Geographic region where the customer’s headquarters is located. | character varying(20) | Customers |

---

# Table: quotetobooking.dim_date

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_date |
| Business Term | Date Dimension |
| Business Definition | Stores calendar and fiscal date attributes used to analyze bookings over time by date, month, quarter, and year. |
| Business Category | Time |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| date_key | Date Key | Numeric surrogate or formatted date key used to join time attributes to booking transactions. | integer | Time |
| full_date | Full Date | Actual calendar date represented by the date record. | date | Time |
| month_name | Month Name | Name of the calendar month for the date. | character varying(12) | Time |
| calendar_year | Calendar Year | Calendar year corresponding to the date. | integer | Time |
| fiscal_year | Fiscal Year | Fiscal year corresponding to the date based on business reporting conventions. | character varying(6) | Time |
| fiscal_quarter | Fiscal Quarter | Fiscal quarter corresponding to the date. | character varying(10) | Time |
| fiscal_period_seq | Fiscal Period Sequence | Sequential number representing the fiscal reporting period in order. | integer | Time |

---

# Table: quotetobooking.dim_geography

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_geography |
| Business Term | Geography Dimension |
| Business Definition | Stores geographic classifications used to analyze bookings by region, theater, and country. |
| Business Category | Geography |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| geography_key | Geography Key | Unique surrogate key for the geography record used to join geographic attributes to booking transactions. | integer | Geography |
| region | Region | High-level geographic reporting region for the booking or customer coverage area. | character varying(20) | Geography |
| theater | Theater | Sub-regional sales theater or operating area within a broader region. | character varying(30) | Geography |
| country | Country | Country associated with the geography record. | character varying(40) | Geography |

---

# Table: quotetobooking.dim_partner

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_partner |
| Business Term | Partner Dimension |
| Business Definition | Stores channel partner attributes used to analyze bookings by partner identity, partner type, tier, and route to market. |
| Business Category | Partners |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| partner_key | Partner Key | Unique surrogate key for the partner record used to join partner details to booking transactions. | integer | Partners |
| partner_id | Partner Identifier | Business identifier assigned to the partner account. | character varying(20) | Partners |
| partner_name | Partner Name | Name of the partner organization involved in the sale. | character varying(60) | Partners |
| partner_type | Partner Type | Classification of the partner, such as distributor, reseller, direct, or systems integrator. | character varying(30) | Partners |
| partner_tier | Partner Tier | Program tier or status level assigned to the partner. | character varying(30) | Partners |
| route_to_market | Route to Market | Sales channel path through which the booking is transacted, such as direct, reseller, or two-tier. | character varying(20) | Partners |

---

# Table: quotetobooking.dim_product

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_product |
| Business Term | Product Dimension |
| Business Definition | Stores product master data used to analyze bookings by product, family, technology domain, offer type, and business entity. |
| Business Category | Products |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| product_key | Product Key | Unique surrogate key for the product record used to join product details to booking transactions. | integer | Products |
| product_id | Product Identifier | Business identifier or SKU assigned to the product or offer. | character varying(30) | Products |
| product_name | Product Name | Descriptive name of the product or solution being booked. | character varying(80) | Products |
| product_family | Product Family | Higher-level grouping of related products within the portfolio. | character varying(30) | Products |
| technology_domain | Technology Domain | Technology area or solution domain to which the product belongs. | character varying(40) | Products |
| offer_type | Offer Type | Commercial offer classification, such as hardware, SaaS subscription, or software subscription. | character varying(30) | Products |
| business_entity | Business Entity | Internal business unit or portfolio grouping responsible for the product. | character varying(30) | Products |

---

# Table: quotetobooking.dim_sales_rep

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_sales_rep |
| Business Term | Sales Representative Dimension |
| Business Definition | Stores sales representative attributes used to analyze bookings by seller identity, role, team, and covered segment. |
| Business Category | Sales |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| sales_rep_key | Sales Representative Key | Unique surrogate key for the sales representative record used to join seller details to booking transactions. | integer | Sales |
| rep_id | Sales Representative Identifier | Business identifier assigned to the sales representative. | character varying(20) | Sales |
| rep_name | Sales Representative Name | Full name of the sales representative associated with the booking. | character varying(60) | Sales |
| sales_role | Sales Role | Job role or selling responsibility of the sales representative. | character varying(40) | Sales |
| sales_team | Sales Team | Sales team or organizational unit to which the sales representative belongs. | character varying(40) | Sales |
| segment_covered | Covered Segment | Customer segment or market segment covered by the sales representative. | character varying(30) | Sales |

---

# Table: quotetobooking.fact_bookings

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.fact_bookings |
| Business Term | Bookings Fact |
| Business Definition | Stores transactional booking records for customer orders, including associated dimensions, quantities, pricing, discounts, and contract value metrics. |
| Business Category | Sales Transactions |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| booking_id | Booking Identifier | Unique identifier for the booking transaction record. | integer | Sales Transactions |
| order_number | Order Number | Business order number associated with the booking transaction. | character varying(20) | Sales Transactions |
| order_line_number | Order Line Number | Line number within the order identifying the specific booked item or service. | integer | Sales Transactions |
| date_key | Booking Date Key | Foreign key linking the booking to the date dimension. | integer | Time |
| customer_key | Customer Key | Foreign key linking the booking to the customer dimension. | integer | Customers |
| product_key | Product Key | Foreign key linking the booking to the product dimension. | integer | Products |
| partner_key | Partner Key | Foreign key linking the booking to the partner dimension. | integer | Partners |
| geography_key | Geography Key | Foreign key linking the booking to the geography dimension. | integer | Geography |
| sales_rep_key | Sales Representative Key | Foreign key linking the booking to the sales representative dimension. | integer | Sales |
| contract_key | Contract Key | Foreign key linking the booking to the contract dimension. | integer | Contracts |
| booking_type | Booking Type | Indicates whether the booking is a new sale or a renewal. | character varying(15) | Sales Transactions |
| is_renewal | Renewal Indicator | Indicates whether the booking transaction is a renewal record, typically using 1 for yes and 0 for no. | integer | Sales Transactions |
| quantity | Quantity | Number of units, licenses, or items included in the booking line. | integer | Sales Transactions |
| unit_list_price_usd | Unit List Price USD | Standard list price per unit in US dollars before discount. | numeric(12,2) | Pricing |
| discount_pct | Discount Percentage | Discount rate applied to the booked item relative to list price. | numeric(5,2) | Pricing |
| booking_amount_usd | Booking Amount USD | Total booked revenue amount in US dollars after pricing and discount considerations. | numeric(14,2) | Revenue |
| acv_usd | Annual Contract Value USD | Annualized contract value of the booking in US dollars. | numeric(14,2) | Revenue |
| tcv_usd | Total Contract Value USD | Total contract value of the booking in US dollars across the full contract term. | numeric(14,2) | Revenue |
