# Business Domain Context

**Domain Name:** Sales Bookings and Revenue Analytics

This domain captures completed customer booking transactions for enterprise products and subscription services and supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods. The model follows a star schema where `fact_bookings` stores transactional booking measures and the dimension tables provide descriptive business context.

---

# Table: quotetobooking.dim_contract

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_contract |
| Business Term | Contract |
| Business Definition | Contains the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and service coverage. |
| Business Category | Sales Agreement Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| contract_key | Contract Key | Surrogate key that uniquely identifies a contract record in the contract dimension. | integer | Identifier |
| contract_type | Contract Type | Describes the type of commercial agreement or support contract tied to the booking, such as SaaS Subscription or Enterprise Agreement. | character varying(40) | Contract Classification |
| term_months | Contract Term Months | Number of months covered by the contract or subscription term. | integer | Contract Duration |
| auto_renew_flag | Auto Renew Flag | Indicates whether the contract is configured to renew automatically. | character(1) | Renewal Indicator |
| coverage_level | Coverage Level | Describes the service or support coverage level provided under the contract. | character varying(20) | Service Coverage |

---

# Table: quotetobooking.dim_customer

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_customer |
| Business Term | Customer |
| Business Definition | Contains descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location. |
| Business Category | Customer Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| customer_key | Customer Key | Surrogate key that uniquely identifies a customer record in the customer dimension. | integer | Identifier |
| customer_id | Customer ID | Business identifier assigned to the customer account. | character varying(20) | Business Identifier |
| customer_name | Customer Name | Official name of the customer organization. | character varying(80) | Customer Profile |
| segment | Customer Segment | Market segment to which the customer belongs, such as Enterprise, Public Sector, or Service Provider. | character varying(30) | Market Segment |
| industry | Industry | Industry classification of the customer organization. | character varying(40) | Industry Classification |
| account_tier | Account Tier | Strategic importance or service tier assigned to the customer account. | character varying(20) | Account Classification |
| hq_country | Headquarters Country | Country where the customer organization's headquarters is located. | character varying(40) | Customer Geography |
| hq_region | Headquarters Region | Global region where the customer organization's headquarters is located. | character varying(20) | Customer Geography |

---

# Table: quotetobooking.dim_date

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_date |
| Business Term | Date |
| Business Definition | Contains calendar and fiscal time attributes used to analyze bookings across reporting periods. |
| Business Category | Time Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| date_key | Date Key | Surrogate-style date identifier used to join booking records to the date dimension. | integer | Identifier |
| full_date | Full Date | Actual calendar date represented by the date record. | date | Calendar Attribute |
| month_name | Month Name | Name of the calendar month for the date. | character varying(12) | Calendar Attribute |
| calendar_year | Calendar Year | Four-digit calendar year for the date. | integer | Calendar Attribute |
| fiscal_year | Fiscal Year | Fiscal year label used for business reporting. | character varying(6) | Fiscal Attribute |
| fiscal_quarter | Fiscal Quarter | Fiscal quarter label used for financial and sales analysis. | character varying(10) | Fiscal Attribute |
| fiscal_period_seq | Fiscal Period Sequence | Sequential position of the fiscal period within the modeled reporting timeline. | integer | Fiscal Attribute |

---

# Table: quotetobooking.dim_geography

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_geography |
| Business Term | Geography |
| Business Definition | Contains geographic reporting attributes used to analyze bookings by region, theater, and country. |
| Business Category | Geography Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| geography_key | Geography Key | Surrogate key that uniquely identifies a geography record in the geography dimension. | integer | Identifier |
| region | Region | High-level global sales region used for reporting, such as Americas, EMEA, or APJC. | character varying(20) | Geographic Hierarchy |
| theater | Theater | Subregional sales theater within a broader region. | character varying(30) | Geographic Hierarchy |
| country | Country | Country associated with the geography record. | character varying(40) | Geographic Attribute |

---

# Table: quotetobooking.dim_partner

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_partner |
| Business Term | Partner |
| Business Definition | Contains descriptive information about channel and direct partners involved in fulfilling customer bookings. |
| Business Category | Partner Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| partner_key | Partner Key | Surrogate key that uniquely identifies a partner record in the partner dimension. | integer | Identifier |
| partner_id | Partner ID | Business identifier assigned to the partner. | character varying(20) | Business Identifier |
| partner_name | Partner Name | Name of the partner organization associated with the booking. | character varying(60) | Partner Profile |
| partner_type | Partner Type | Classification of the partner, such as distributor, reseller, systems integrator, or direct. | character varying(30) | Partner Classification |
| partner_tier | Partner Tier | Tier or program level assigned to the partner. | character varying(30) | Partner Classification |
| route_to_market | Route to Market | Sales channel path through which the product or service is sold, such as Direct, Reseller, or Two-Tier. | character varying(20) | Channel Model |

---

# Table: quotetobooking.dim_product

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_product |
| Business Term | Product |
| Business Definition | Contains descriptive information about products and subscription offers included in booking transactions. |
| Business Category | Product Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| product_key | Product Key | Surrogate key that uniquely identifies a product record in the product dimension. | integer | Identifier |
| product_id | Product ID | Business identifier or SKU assigned to the product or offer. | character varying(30) | Business Identifier |
| product_name | Product Name | Descriptive name of the product or service offering. | character varying(80) | Product Profile |
| product_family | Product Family | Product family grouping used to organize related offerings. | character varying(30) | Product Classification |
| technology_domain | Technology Domain | Technology area or solution domain to which the product belongs. | character varying(40) | Technology Classification |
| offer_type | Offer Type | Commercial offer model for the product, such as Hardware, SaaS Subscription, or Software Subscription. | character varying(30) | Offer Classification |
| business_entity | Business Entity | Internal business portfolio or organizational entity associated with the product. | character varying(30) | Portfolio Classification |

---

# Table: quotetobooking.dim_sales_rep

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_sales_rep |
| Business Term | Sales Representative |
| Business Definition | Contains descriptive information about sales personnel responsible for managing customer relationships and booking activity. |
| Business Category | Sales Organization Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| sales_rep_key | Sales Representative Key | Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. | integer | Identifier |
| rep_id | Sales Representative ID | Business identifier assigned to the sales representative. | character varying(20) | Business Identifier |
| rep_name | Sales Representative Name | Full name of the sales representative. | character varying(60) | Sales Profile |
| sales_role | Sales Role | Job role or commercial responsibility of the sales representative. | character varying(40) | Sales Organization |
| sales_team | Sales Team | Sales team or organizational unit to which the sales representative belongs. | character varying(40) | Sales Organization |
| segment_covered | Segment Covered | Customer segment primarily covered by the sales representative. | character varying(30) | Coverage Model |

---

# Table: quotetobooking.fact_bookings

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.fact_bookings |
| Business Term | Booking Transaction |
| Business Definition | Stores individual completed sales booking transactions and associated financial measures used for revenue and performance analysis. |
| Business Category | Sales Fact |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| booking_id | Booking ID | Unique identifier for an individual booking transaction record. | integer | Identifier |
| order_number | Order Number | Business order number associated with the booking transaction. | character varying(20) | Transaction Identifier |
| order_line_number | Order Line Number | Line number within the order that identifies the booked item or service entry. | integer | Transaction Detail |
| date_key | Booking Date Key | Reference to the date dimension representing when the booking was recorded. | integer | Foreign Key |
| customer_key | Customer Key | Reference to the customer associated with the booking transaction. | integer | Foreign Key |
| product_key | Product Key | Reference to the product or offer included in the booking transaction. | integer | Foreign Key |
| partner_key | Partner Key | Reference to the partner involved in the booking transaction. | integer | Foreign Key |
| geography_key | Geography Key | Reference to the geography associated with the booking transaction. | integer | Foreign Key |
| sales_rep_key | Sales Representative Key | Reference to the sales representative responsible for the booking. | integer | Foreign Key |
| contract_key | Contract Key | Reference to the contract terms associated with the booking. | integer | Foreign Key |
| booking_type | Booking Type | Indicates the business type of the booking, such as New or Renewal. | character varying(15) | Transaction Classification |
| is_renewal | Renewal Indicator | Indicates whether the booking transaction is a renewal booking. | integer | Renewal Indicator |
| quantity | Quantity Sold | Number of units, licenses, or subscriptions included in the booking transaction. | integer | Volume Measure |
| unit_list_price_usd | Unit List Price USD | Standard list price per unit in U.S. dollars before discounts. | numeric(12,2) | Pricing Measure |
| discount_pct | Discount Percentage | Discount rate applied to the list price for the booking transaction. | numeric(5,2) | Pricing Measure |
| booking_amount_usd | Booking Amount USD | Total booked transaction amount in U.S. dollars after pricing adjustments. | numeric(14,2) | Revenue Measure |
| acv_usd | Annual Contract Value USD | Annualized contract value of the booking in U.S. dollars. | numeric(14,2) | Revenue Measure |
| tcv_usd | Total Contract Value USD | Total contract value of the booking across the full contract term in U.S. dollars. | numeric(14,2) | Revenue Measure |
