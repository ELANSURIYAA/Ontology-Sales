# Business Domain Context

Sales Bookings and Revenue Analytics covers completed customer booking transactions for enterprise networking, security, collaboration, observability, and software subscription products. The model supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods. It follows a star schema in which `fact_bookings` stores booking transactions and the dimension tables provide descriptive business context for reporting, forecasting, renewal tracking, and executive decision-making.

# Table: quotetobooking.dim_contract

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_contract |
| Business Term | Contract |
| Business Definition | Stores the commercial agreement attributes associated with a booking, including contract type, duration, renewal behavior, and coverage level. |
| Business Category | Contract Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| contract_key | Contract Key | Unique surrogate identifier for a contract record used to link contracts to booking transactions. | INTEGER | Contract Management |
| contract_type | Contract Type | Type of commercial agreement or service contract associated with the booking, such as Enterprise Agreement or SaaS Subscription. | VARCHAR(40) | Contract Management |
| term_months | Contract Term Months | Number of months covered by the contract term. | INTEGER | Contract Management |
| auto_renew_flag | Auto Renew Flag | Indicates whether the contract is set to renew automatically at the end of its term. | CHARACTER(1) | Contract Management |
| coverage_level | Coverage Level | Service or support coverage level provided under the contract. | VARCHAR(20) | Contract Management |

---

# Table: quotetobooking.dim_customer

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_customer |
| Business Term | Customer |
| Business Definition | Stores customer master data used to analyze bookings by account, segment, industry, and headquarters location. |
| Business Category | Customer Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| customer_key | Customer Key | Unique surrogate identifier for a customer record used to join customers to booking transactions. | INTEGER | Customer Management |
| customer_id | Customer ID | Business identifier assigned to the customer account. | VARCHAR(20) | Customer Management |
| customer_name | Customer Name | Name of the customer account or organization making the purchase. | VARCHAR(80) | Customer Management |
| segment | Customer Segment | Market segment to which the customer belongs, such as Enterprise, Service Provider, or Public Sector. | VARCHAR(30) | Customer Management |
| industry | Industry | Primary industry classification of the customer. | VARCHAR(40) | Customer Management |
| account_tier | Account Tier | Strategic tier assigned to the customer account for sales prioritization and coverage. | VARCHAR(20) | Customer Management |
| hq_country | Headquarters Country | Country where the customer’s headquarters is located. | VARCHAR(40) | Customer Management |
| hq_region | Headquarters Region | Broad geographic region where the customer’s headquarters is located. | VARCHAR(20) | Customer Management |

---

# Table: quotetobooking.dim_date

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_date |
| Business Term | Date |
| Business Definition | Stores calendar and fiscal date attributes used to analyze booking transactions over time. |
| Business Category | Time Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| date_key | Date Key | Unique numeric identifier for the date record, typically formatted as YYYYMMDD. | INTEGER | Time Management |
| full_date | Full Date | Actual calendar date represented by the date record. | DATE | Time Management |
| month_name | Month Name | Name of the calendar month for the date. | VARCHAR(12) | Time Management |
| calendar_year | Calendar Year | Calendar year associated with the date. | INTEGER | Time Management |
| fiscal_year | Fiscal Year | Fiscal year used for business reporting and performance analysis. | VARCHAR(6) | Time Management |
| fiscal_quarter | Fiscal Quarter | Fiscal quarter used for financial and sales reporting. | VARCHAR(10) | Time Management |
| fiscal_period_seq | Fiscal Period Sequence | Sequential number representing the fiscal period order within the reporting timeline. | INTEGER | Time Management |

---

# Table: quotetobooking.dim_geography

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_geography |
| Business Term | Geography |
| Business Definition | Stores geographic reporting attributes used to analyze bookings by region, theater, and country. |
| Business Category | Geography Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| geography_key | Geography Key | Unique surrogate identifier for a geography record used to join geography to booking transactions. | INTEGER | Geography Management |
| region | Region | High-level sales region used for reporting and performance analysis. | VARCHAR(20) | Geography Management |
| theater | Theater | Intermediate sales geography grouping within a region. | VARCHAR(30) | Geography Management |
| country | Country | Country associated with the geography record. | VARCHAR(40) | Geography Management |

---

# Table: quotetobooking.dim_partner

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_partner |
| Business Term | Partner |
| Business Definition | Stores channel partner master data used to analyze indirect and direct sales routes, partner roles, and partner performance. |
| Business Category | Partner Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| partner_key | Partner Key | Unique surrogate identifier for a partner record used to join partners to booking transactions. | INTEGER | Partner Management |
| partner_id | Partner ID | Business identifier assigned to the partner account. | VARCHAR(20) | Partner Management |
| partner_name | Partner Name | Name of the distributor, reseller, systems integrator, or direct partner involved in the sale. | VARCHAR(60) | Partner Management |
| partner_type | Partner Type | Classification of the partner based on its business role, such as distributor or value-added reseller. | VARCHAR(30) | Partner Management |
| partner_tier | Partner Tier | Tier or accreditation level assigned to the partner. | VARCHAR(30) | Partner Management |
| route_to_market | Route to Market | Sales channel path through which the product or service is sold, such as Direct, Reseller, or Two-Tier. | VARCHAR(20) | Partner Management |

---

# Table: quotetobooking.dim_product

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_product |
| Business Term | Product |
| Business Definition | Stores product master data used to analyze bookings across product families, technology domains, offer types, and business entities. |
| Business Category | Product Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| product_key | Product Key | Unique surrogate identifier for a product record used to join products to booking transactions. | INTEGER | Product Management |
| product_id | Product ID | Business identifier or SKU assigned to the product or service offering. | VARCHAR(30) | Product Management |
| product_name | Product Name | Descriptive name of the product or service sold. | VARCHAR(80) | Product Management |
| product_family | Product Family | Higher-level grouping of related products within the portfolio. | VARCHAR(30) | Product Management |
| technology_domain | Technology Domain | Technology area or solution domain to which the product belongs. | VARCHAR(40) | Product Management |
| offer_type | Offer Type | Commercial offer model for the product, such as Hardware, SaaS Subscription, or Software Subscription. | VARCHAR(30) | Product Management |
| business_entity | Business Entity | Internal business portfolio or organizational entity responsible for the product. | VARCHAR(30) | Product Management |

---

# Table: quotetobooking.dim_sales_rep

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_sales_rep |
| Business Term | Sales Representative |
| Business Definition | Stores sales representative attributes used to analyze bookings by seller, sales role, team, and covered segment. |
| Business Category | Sales Performance |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| sales_rep_key | Sales Representative Key | Unique surrogate identifier for a sales representative record used to join sellers to booking transactions. | INTEGER | Sales Performance |
| rep_id | Sales Representative ID | Business identifier assigned to the sales representative. | VARCHAR(20) | Sales Performance |
| rep_name | Sales Representative Name | Full name of the sales representative managing the customer or opportunity. | VARCHAR(60) | Sales Performance |
| sales_role | Sales Role | Role or title of the sales representative within the sales organization. | VARCHAR(40) | Sales Performance |
| sales_team | Sales Team | Sales team or organizational unit to which the representative belongs. | VARCHAR(40) | Sales Performance |
| segment_covered | Covered Segment | Customer segment for which the sales representative is responsible. | VARCHAR(30) | Sales Performance |

---

# Table: quotetobooking.fact_bookings

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.fact_bookings |
| Business Term | Booking Transaction |
| Business Definition | Stores individual completed sales booking transactions and related financial measures for revenue, contract, customer, partner, product, geography, and sales analysis. |
| Business Category | Sales Transactions |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| booking_id | Booking ID | Unique identifier for an individual booking transaction record. | INTEGER | Sales Transactions |
| order_number | Order Number | Sales order number associated with the booking transaction. | VARCHAR(20) | Sales Transactions |
| order_line_number | Order Line Number | Line number within the sales order identifying the specific booked item. | INTEGER | Sales Transactions |
| date_key | Booking Date Key | Reference to the date dimension representing when the booking was recorded. | INTEGER | Sales Transactions |
| customer_key | Customer Key | Reference to the customer associated with the booking transaction. | INTEGER | Sales Transactions |
| product_key | Product Key | Reference to the product or service booked in the transaction. | INTEGER | Sales Transactions |
| partner_key | Partner Key | Reference to the partner involved in fulfilling or routing the sale. | INTEGER | Sales Transactions |
| geography_key | Geography Key | Reference to the geography used for booking reporting and analysis. | INTEGER | Sales Transactions |
| sales_rep_key | Sales Representative Key | Reference to the sales representative responsible for the booking. | INTEGER | Sales Transactions |
| contract_key | Contract Key | Reference to the contract or commercial agreement associated with the booking. | INTEGER | Sales Transactions |
| booking_type | Booking Type | Classification of the booking event, such as New or Renewal. | VARCHAR(15) | Sales Transactions |
| is_renewal | Renewal Indicator | Indicates whether the booking represents a renewal transaction. | INTEGER | Sales Transactions |
| quantity | Quantity Sold | Number of product units, licenses, or service quantities included in the booking. | INTEGER | Sales Transactions |
| unit_list_price_usd | Unit List Price USD | Standard list price per unit in U.S. dollars before discounts. | NUMERIC(12,2) | Sales Transactions |
| discount_pct | Discount Percentage | Discount rate applied to the booked product or service. | NUMERIC(5,2) | Sales Transactions |
| booking_amount_usd | Booking Amount USD | Total booked revenue amount in U.S. dollars after applied pricing and discounts. | NUMERIC(14,2) | Sales Transactions |
| acv_usd | Annual Contract Value USD | Annualized contract value of the booking in U.S. dollars. | NUMERIC(14,2) | Sales Transactions |
| tcv_usd | Total Contract Value USD | Total contract value of the booking over the full contract term in U.S. dollars. | NUMERIC(14,2) | Sales Transactions |