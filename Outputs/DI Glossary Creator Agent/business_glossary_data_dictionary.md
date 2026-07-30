# Business Domain Context

Sales Bookings and Revenue Analytics

This domain represents sales booking operations for enterprise networking, security, collaboration, observability, and software subscription products. It captures completed customer bookings and supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods.

# Table: quotetobooking.dim_contract

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_contract |
| Business Term | Contract |
| Business Definition | Describes the commercial agreement or service coverage terms associated with a booking, including contract type, duration, renewal behavior, and support coverage level. |
| Business Category | Contract Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| contract_key | Contract Key | Surrogate key that uniquely identifies a contract record in the contract dimension. | integer | Contract Management |
| contract_type | Contract Type | Type of commercial agreement or support entitlement, such as Enterprise Agreement, SaaS Subscription, or Solution Support. | character varying(40) | Contract Management |
| term_months | Contract Term Months | Number of months covered by the contract or subscription term. | integer | Contract Management |
| auto_renew_flag | Auto Renewal Flag | Indicator showing whether the contract is set to renew automatically at the end of its term. | character(1) | Contract Management |
| coverage_level | Coverage Level | Service or support coverage level provided under the contract. | character varying(20) | Contract Management |

---

# Table: quotetobooking.dim_customer

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_customer |
| Business Term | Customer |
| Business Definition | Stores descriptive information about customers that place orders, including identity, segment, industry, account tier, and headquarters location. |
| Business Category | Customer Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| customer_key | Customer Key | Surrogate key that uniquely identifies a customer record in the customer dimension. | integer | Customer Management |
| customer_id | Customer ID | Business identifier assigned to the customer account. | character varying(20) | Customer Management |
| customer_name | Customer Name | Official name of the customer organization. | character varying(80) | Customer Management |
| segment | Customer Segment | Market segment the customer belongs to, such as Enterprise, Service Provider, or Public Sector. | character varying(30) | Customer Management |
| industry | Industry | Industry classification of the customer organization. | character varying(40) | Customer Management |
| account_tier | Account Tier | Strategic importance or service tier assigned to the customer account. | character varying(20) | Customer Management |
| hq_country | Headquarters Country | Country where the customer organization's headquarters is located. | character varying(40) | Customer Management |
| hq_region | Headquarters Region | Broad geographic region of the customer organization's headquarters. | character varying(20) | Customer Management |

---

# Table: quotetobooking.dim_date

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_date |
| Business Term | Date |
| Business Definition | Provides calendar and fiscal time attributes used to analyze bookings across reporting periods, years, quarters, and months. |
| Business Category | Time Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| date_key | Date Key | Surrogate date key used to join booking records to the date dimension. | integer | Time Management |
| full_date | Full Date | Actual calendar date represented by the date record. | date | Time Management |
| month_name | Month Name | Name of the calendar month for the date. | character varying(12) | Time Management |
| calendar_year | Calendar Year | Calendar year associated with the date. | integer | Time Management |
| fiscal_year | Fiscal Year | Fiscal year used for financial and sales reporting. | character varying(6) | Time Management |
| fiscal_quarter | Fiscal Quarter | Fiscal quarter used for period-based reporting and analysis. | character varying(10) | Time Management |
| fiscal_period_seq | Fiscal Period Sequence | Sequential number representing the fiscal reporting period in order. | integer | Time Management |

---

# Table: quotetobooking.dim_geography

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_geography |
| Business Term | Geography |
| Business Definition | Stores geographic sales territory attributes used to analyze bookings by region, theater, and country. |
| Business Category | Geography |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| geography_key | Geography Key | Surrogate key that uniquely identifies a geography record in the geography dimension. | integer | Geography |
| region | Sales Region | High-level geographic region used for sales reporting, such as Americas, EMEA, or APJC. | character varying(20) | Geography |
| theater | Sales Theater | Intermediate sales territory grouping within a region. | character varying(30) | Geography |
| country | Country | Country associated with the geography record. | character varying(40) | Geography |

---

# Table: quotetobooking.dim_partner

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_partner |
| Business Term | Partner |
| Business Definition | Stores information about direct and indirect sales partners involved in fulfilling customer bookings, including partner identity, type, tier, and route to market. |
| Business Category | Partner Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| partner_key | Partner Key | Surrogate key that uniquely identifies a partner record in the partner dimension. | integer | Partner Management |
| partner_id | Partner ID | Business identifier assigned to the partner organization. | character varying(20) | Partner Management |
| partner_name | Partner Name | Official name of the partner organization. | character varying(60) | Partner Management |
| partner_type | Partner Type | Classification of the partner, such as distributor, reseller, systems integrator, or direct channel. | character varying(30) | Partner Management |
| partner_tier | Partner Tier | Program tier or status level assigned to the partner. | character varying(30) | Partner Management |
| route_to_market | Route to Market | Sales channel path through which the product or service is sold to the customer. | character varying(20) | Partner Management |

---

# Table: quotetobooking.dim_product

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_product |
| Business Term | Product |
| Business Definition | Stores descriptive information about products and offers sold to customers, including product identity, family, technology domain, offer type, and business entity. |
| Business Category | Product Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| product_key | Product Key | Surrogate key that uniquely identifies a product record in the product dimension. | integer | Product Management |
| product_id | Product ID | Business identifier or SKU assigned to the product or offer. | character varying(30) | Product Management |
| product_name | Product Name | Descriptive name of the product or service offering. | character varying(80) | Product Management |
| product_family | Product Family | Higher-level grouping of related products within the portfolio. | character varying(30) | Product Management |
| technology_domain | Technology Domain | Technology area or solution domain the product belongs to. | character varying(40) | Product Management |
| offer_type | Offer Type | Commercial offer classification, such as hardware, software subscription, or SaaS subscription. | character varying(30) | Product Management |
| business_entity | Business Entity | Internal business portfolio or organizational unit associated with the product. | character varying(30) | Product Management |

---

# Table: quotetobooking.dim_sales_rep

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_sales_rep |
| Business Term | Sales Representative |
| Business Definition | Stores information about the sales person responsible for managing customer relationships and booking transactions, including role, team, and segment coverage. |
| Business Category | Sales Organization |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| sales_rep_key | Sales Representative Key | Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. | integer | Sales Organization |
| rep_id | Sales Representative ID | Business identifier assigned to the sales representative. | character varying(20) | Sales Organization |
| rep_name | Sales Representative Name | Full name of the sales representative. | character varying(60) | Sales Organization |
| sales_role | Sales Role | Job role or selling responsibility of the sales representative. | character varying(40) | Sales Organization |
| sales_team | Sales Team | Team or organizational unit the sales representative belongs to. | character varying(40) | Sales Organization |
| segment_covered | Segment Covered | Customer segment or market segment covered by the sales representative. | character varying(30) | Sales Organization |

---

# Table: quotetobooking.fact_bookings

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.fact_bookings |
| Business Term | Booking Transaction |
| Business Definition | Captures individual completed sales booking transactions and their associated financial measures, quantities, renewal status, and links to related business dimensions. |
| Business Category | Sales Performance |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| booking_id | Booking ID | Unique identifier for an individual booking transaction record. | integer | Sales Performance |
| order_number | Order Number | Sales order number associated with the booking transaction. | character varying(20) | Sales Performance |
| order_line_number | Order Line Number | Line number within the sales order representing the booked item or service. | integer | Sales Performance |
| date_key | Booking Date Key | Foreign key linking the booking transaction to the reporting date dimension. | integer | Sales Performance |
| customer_key | Customer Key | Foreign key linking the booking transaction to the customer dimension. | integer | Sales Performance |
| product_key | Product Key | Foreign key linking the booking transaction to the product dimension. | integer | Sales Performance |
| partner_key | Partner Key | Foreign key linking the booking transaction to the partner dimension. | integer | Sales Performance |
| geography_key | Geography Key | Foreign key linking the booking transaction to the geography dimension. | integer | Sales Performance |
| sales_rep_key | Sales Representative Key | Foreign key linking the booking transaction to the sales representative dimension. | integer | Sales Performance |
| contract_key | Contract Key | Foreign key linking the booking transaction to the contract dimension. | integer | Sales Performance |
| booking_type | Booking Type | Type of booking event, such as new business or renewal. | character varying(15) | Sales Performance |
| is_renewal | Renewal Indicator | Indicator showing whether the booking transaction is a renewal. | integer | Sales Performance |
| quantity | Quantity Sold | Number of units, licenses, or services booked in the transaction. | integer | Sales Performance |
| unit_list_price_usd | Unit List Price USD | Standard list price per unit in US dollars before discounts. | numeric(12,2) | Sales Performance |
| discount_pct | Discount Percentage | Discount applied to the booked item or service, expressed as a percentage of list price. | numeric(5,2) | Sales Performance |
| booking_amount_usd | Booking Amount USD | Total booked sales amount in US dollars after pricing and discount adjustments. | numeric(14,2) | Sales Performance |
| acv_usd | Annual Contract Value USD | Annualized contract value of the booking in US dollars. | numeric(14,2) | Sales Performance |
| tcv_usd | Total Contract Value USD | Total contract value of the booking over the full contract term in US dollars. | numeric(14,2) | Sales Performance |
