# Business Domain Context

Sales Bookings and Revenue Analytics is a business domain focused on tracking completed customer bookings for enterprise networking, security, collaboration, observability, and software subscription products. The model supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods. It captures key financial measures such as booking amount, annual contract value, total contract value, quantity sold, unit list price, discount percentage, booking type, and renewal indicator.

# Table: quotetobooking.dim_contract

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_contract |
| Business Term | Contract Dimension |
| Business Definition | Stores contract and service agreement attributes used to classify bookings by contract type, term, renewal behavior, and coverage level. |
| Business Category | Contract Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| contract_key | Contract Key | Surrogate key that uniquely identifies a contract record in the contract dimension. | integer | Contract Management |
| contract_type | Contract Type | Type of commercial agreement associated with the booking, such as Enterprise Agreement, SaaS Subscription, or support contract. | character varying(40) | Contract Management |
| term_months | Contract Term Months | Number of months covered by the contract or service agreement. | integer | Contract Management |
| auto_renew_flag | Auto Renew Flag | Indicator showing whether the contract is configured to renew automatically. | character(1) | Contract Management |
| coverage_level | Coverage Level | Service or support coverage level provided under the contract. | character varying(20) | Contract Management |

---

# Table: quotetobooking.dim_customer

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_customer |
| Business Term | Customer Dimension |
| Business Definition | Stores descriptive customer attributes used to analyze bookings by customer identity, segment, industry, account tier, and headquarters location. |
| Business Category | Customer Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| customer_key | Customer Key | Surrogate key that uniquely identifies a customer record in the customer dimension. | integer | Customer Management |
| customer_id | Customer ID | Business identifier assigned to the customer account. | character varying(20) | Customer Management |
| customer_name | Customer Name | Name of the customer organization that placed the order. | character varying(80) | Customer Management |
| segment | Customer Segment | Market segment to which the customer belongs, such as Enterprise, Service Provider, or Public Sector. | character varying(30) | Customer Management |
| industry | Industry | Industry classification of the customer organization. | character varying(40) | Customer Management |
| account_tier | Account Tier | Strategic importance or tier assigned to the customer account. | character varying(20) | Customer Management |
| hq_country | Headquarters Country | Country where the customer organization's headquarters is located. | character varying(40) | Customer Management |
| hq_region | Headquarters Region | Global region where the customer headquarters is located. | character varying(20) | Customer Management |

---

# Table: quotetobooking.dim_date

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_date |
| Business Term | Date Dimension |
| Business Definition | Stores calendar and fiscal date attributes used to analyze bookings across time periods, fiscal years, quarters, and months. |
| Business Category | Time Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| date_key | Date Key | Numeric surrogate key representing a specific calendar date. | integer | Time Management |
| full_date | Full Date | Actual calendar date represented by the date record. | date | Time Management |
| month_name | Month Name | Name of the calendar month for the date. | character varying(12) | Time Management |
| calendar_year | Calendar Year | Four-digit calendar year of the date. | integer | Time Management |
| fiscal_year | Fiscal Year | Fiscal year used for business reporting and financial analysis. | character varying(6) | Time Management |
| fiscal_quarter | Fiscal Quarter | Fiscal quarter associated with the date for reporting purposes. | character varying(10) | Time Management |
| fiscal_period_seq | Fiscal Period Sequence | Sequential number representing the fiscal period order in the reporting calendar. | integer | Time Management |

---

# Table: quotetobooking.dim_geography

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_geography |
| Business Term | Geography Dimension |
| Business Definition | Stores geographic attributes used to analyze bookings by region, theater, and country. |
| Business Category | Geography |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| geography_key | Geography Key | Surrogate key that uniquely identifies a geography record in the geography dimension. | integer | Geography |
| region | Region | Broad global sales region associated with the booking, such as Americas, EMEA, or APJC. | character varying(20) | Geography |
| theater | Theater | Sales theater or sub-region used for operational reporting within a region. | character varying(30) | Geography |
| country | Country | Country associated with the geography record. | character varying(40) | Geography |

---

# Table: quotetobooking.dim_partner

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_partner |
| Business Term | Partner Dimension |
| Business Definition | Stores channel partner attributes used to analyze bookings by partner identity, partner type, partner tier, and route to market. |
| Business Category | Partner Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| partner_key | Partner Key | Surrogate key that uniquely identifies a partner record in the partner dimension. | integer | Partner Management |
| partner_id | Partner ID | Business identifier assigned to the partner organization. | character varying(20) | Partner Management |
| partner_name | Partner Name | Name of the distributor, reseller, integrator, or direct channel partner involved in the booking. | character varying(60) | Partner Management |
| partner_type | Partner Type | Classification of the partner, such as distributor, value-added reseller, systems integrator, or direct. | character varying(30) | Partner Management |
| partner_tier | Partner Tier | Tier or certification level assigned to the partner in the channel program. | character varying(30) | Partner Management |
| route_to_market | Route to Market | Sales route through which the booking was transacted, such as direct, reseller, or two-tier. | character varying(20) | Partner Management |

---

# Table: quotetobooking.dim_product

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_product |
| Business Term | Product Dimension |
| Business Definition | Stores product and offer attributes used to analyze bookings by product identity, family, technology domain, offer type, and business entity. |
| Business Category | Product Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| product_key | Product Key | Surrogate key that uniquely identifies a product record in the product dimension. | integer | Product Management |
| product_id | Product ID | Business identifier or SKU assigned to the product or subscription offer. | character varying(30) | Product Management |
| product_name | Product Name | Descriptive name of the product, service, or subscription offer. | character varying(80) | Product Management |
| product_family | Product Family | Higher-level grouping of related products within the portfolio. | character varying(30) | Product Management |
| technology_domain | Technology Domain | Technology area to which the product belongs, such as networking, security, or collaboration. | character varying(40) | Product Management |
| offer_type | Offer Type | Commercial offer classification, such as hardware, SaaS subscription, or software subscription. | character varying(30) | Product Management |
| business_entity | Business Entity | Internal business portfolio or organizational entity responsible for the product. | character varying(30) | Product Management |

---

# Table: quotetobooking.dim_sales_rep

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_sales_rep |
| Business Term | Sales Representative Dimension |
| Business Definition | Stores sales representative attributes used to analyze bookings by sales person, role, team, and market segment coverage. |
| Business Category | Sales Organization |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| sales_rep_key | Sales Representative Key | Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. | integer | Sales Organization |
| rep_id | Sales Representative ID | Business identifier assigned to the sales representative. | character varying(20) | Sales Organization |
| rep_name | Sales Representative Name | Full name of the sales representative managing the account or opportunity. | character varying(60) | Sales Organization |
| sales_role | Sales Role | Job role or selling role performed by the sales representative. | character varying(40) | Sales Organization |
| sales_team | Sales Team | Sales team or organization to which the representative belongs. | character varying(40) | Sales Organization |
| segment_covered | Segment Covered | Customer segment primarily covered by the sales representative. | character varying(30) | Sales Organization |

---

# Table: quotetobooking.fact_bookings

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.fact_bookings |
| Business Term | Booking Fact |
| Business Definition | Stores individual booking transactions and their financial measures for analyzing sales performance across customers, products, partners, geographies, contracts, sales representatives, and time. |
| Business Category | Sales Transactions |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| booking_id | Booking ID | Unique identifier for an individual booking transaction. | integer | Sales Transactions |
| order_number | Order Number | Sales order number associated with the booking transaction. | character varying(20) | Sales Transactions |
| order_line_number | Order Line Number | Line number within the sales order that identifies the specific booked item. | integer | Sales Transactions |
| date_key | Date Key | Reference to the date dimension indicating when the booking was recorded. | integer | Time Management |
| customer_key | Customer Key | Reference to the customer associated with the booking. | integer | Customer Management |
| product_key | Product Key | Reference to the product or offer included in the booking. | integer | Product Management |
| partner_key | Partner Key | Reference to the partner involved in fulfilling or transacting the booking. | integer | Partner Management |
| geography_key | Geography Key | Reference to the geography associated with the booking. | integer | Geography |
| sales_rep_key | Sales Representative Key | Reference to the sales representative responsible for the booking. | integer | Sales Organization |
| contract_key | Contract Key | Reference to the contract or commercial agreement associated with the booking. | integer | Contract Management |
| booking_type | Booking Type | Classification of the booking event, such as new business or renewal. | character varying(15) | Sales Transactions |
| is_renewal | Renewal Indicator | Indicator showing whether the booking represents a renewal transaction. | integer | Sales Transactions |
| quantity | Quantity Sold | Number of units, licenses, or subscriptions booked in the transaction. | integer | Sales Transactions |
| unit_list_price_usd | Unit List Price USD | Standard list price per unit in U.S. dollars before discounts. | numeric(12,2) | Pricing |
| discount_pct | Discount Percentage | Discount applied to the list price for the booking line. | numeric(5,2) | Pricing |
| booking_amount_usd | Booking Amount USD | Total booked revenue amount in U.S. dollars for the transaction. | numeric(14,2) | Revenue Metrics |
| acv_usd | Annual Contract Value USD | Annualized contract value in U.S. dollars used for recurring revenue analysis. | numeric(14,2) | Revenue Metrics |
| tcv_usd | Total Contract Value USD | Total contract value in U.S. dollars over the full contract term. | numeric(14,2) | Revenue Metrics |
