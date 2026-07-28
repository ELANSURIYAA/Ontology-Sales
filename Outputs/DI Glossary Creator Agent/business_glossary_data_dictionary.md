# Business Domain Context

**Domain Name:** Sales Bookings and Revenue Analytics

This domain represents sales booking operations for enterprise networking, security, collaboration, observability, and software subscription products. It captures completed customer bookings and supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods.

# Table: QuoteToBooking.dim_contract

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_contract |
| Business Term | Contract |
| Business Definition | Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level. |
| Business Category | Contract Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| contract_key | Contract Key | Surrogate key that uniquely identifies a contract record in the contract dimension. | integer | Technical Identifier |
| contract_type | Contract Type | Describes the type of commercial agreement attached to the booking, such as SaaS subscription, Enterprise Agreement, or support contract. | character varying(40) | Contract Management |
| term_months | Contract Term Months | Indicates the duration of the contract in months. | integer | Contract Management |
| auto_renew_flag | Auto Renew Flag | Indicates whether the contract is set to renew automatically at the end of its term. | character(1) | Renewal Management |
| coverage_level | Coverage Level | Describes the level of service or support coverage provided under the contract. | character varying(20) | Service Coverage |

---

# Table: QuoteToBooking.dim_customer

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_customer |
| Business Term | Customer |
| Business Definition | Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location. |
| Business Category | Customer Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| customer_key | Customer Key | Surrogate key that uniquely identifies a customer record in the customer dimension. | integer | Technical Identifier |
| customer_id | Customer ID | Business identifier assigned to the customer account. | character varying(20) | Customer Management |
| customer_name | Customer Name | Official name of the customer organization that purchased products or services. | character varying(80) | Customer Management |
| segment | Customer Segment | Classifies the customer into a business segment such as Enterprise, Service Provider, or Public Sector. | character varying(30) | Customer Segmentation |
| industry | Industry | Identifies the industry in which the customer operates. | character varying(40) | Customer Segmentation |
| account_tier | Account Tier | Indicates the strategic importance or service tier of the customer account. | character varying(20) | Account Management |
| hq_country | Headquarters Country | Country where the customer organization's headquarters is located. | character varying(40) | Geography |
| hq_region | Headquarters Region | Global region where the customer organization's headquarters is located. | character varying(20) | Geography |

---

# Table: QuoteToBooking.dim_date

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_date |
| Business Term | Date |
| Business Definition | Stores calendar and fiscal date attributes used to analyze bookings over time. |
| Business Category | Time Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| date_key | Date Key | Surrogate or encoded key that uniquely identifies a reporting date in the date dimension. | integer | Technical Identifier |
| full_date | Full Date | Actual calendar date represented by the date record. | date | Time Management |
| month_name | Month Name | Name of the calendar month for the date. | character varying(12) | Time Management |
| calendar_year | Calendar Year | Four-digit calendar year associated with the date. | integer | Time Management |
| fiscal_year | Fiscal Year | Fiscal year used by the business for financial and performance reporting. | character varying(6) | Financial Reporting |
| fiscal_quarter | Fiscal Quarter | Fiscal quarter used by the business for periodic reporting and analysis. | character varying(10) | Financial Reporting |
| fiscal_period_seq | Fiscal Period Sequence | Sequential number representing the fiscal reporting period in ordered time analysis. | integer | Financial Reporting |

---

# Table: QuoteToBooking.dim_geography

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_geography |
| Business Term | Geography |
| Business Definition | Stores geographic attributes used to analyze bookings by sales region, theater, and country. |
| Business Category | Geographic Analysis |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| geography_key | Geography Key | Surrogate key that uniquely identifies a geography record in the geography dimension. | integer | Technical Identifier |
| region | Sales Region | High-level geographic region used for reporting and performance analysis. | character varying(20) | Geographic Analysis |
| theater | Sales Theater | Subregional sales area or theater used to organize market coverage and reporting. | character varying(30) | Geographic Analysis |
| country | Country | Country associated with the geography record. | character varying(40) | Geographic Analysis |

---

# Table: QuoteToBooking.dim_partner

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_partner |
| Business Term | Partner |
| Business Definition | Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market. |
| Business Category | Partner Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| partner_key | Partner Key | Surrogate key that uniquely identifies a partner record in the partner dimension. | integer | Technical Identifier |
| partner_id | Partner ID | Business identifier assigned to the partner organization. | character varying(20) | Partner Management |
| partner_name | Partner Name | Name of the partner organization involved in the transaction. | character varying(60) | Partner Management |
| partner_type | Partner Type | Classifies the partner by operating model, such as distributor, reseller, systems integrator, or direct. | character varying(30) | Partner Classification |
| partner_tier | Partner Tier | Indicates the certification, authorization, or strategic tier assigned to the partner. | character varying(30) | Partner Classification |
| route_to_market | Route to Market | Describes the sales delivery path through which the product or service reached the customer. | character varying(20) | Channel Strategy |

---

# Table: QuoteToBooking.dim_product

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_product |
| Business Term | Product |
| Business Definition | Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity. |
| Business Category | Product Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| product_key | Product Key | Surrogate key that uniquely identifies a product record in the product dimension. | integer | Technical Identifier |
| product_id | Product ID | Business identifier or SKU assigned to the product or offer. | character varying(30) | Product Management |
| product_name | Product Name | Commercial name of the product or subscription offer sold to the customer. | character varying(80) | Product Management |
| product_family | Product Family | Higher-level product grouping used for portfolio and performance analysis. | character varying(30) | Product Classification |
| technology_domain | Technology Domain | Technology area or solution domain to which the product belongs. | character varying(40) | Product Classification |
| offer_type | Offer Type | Indicates whether the item is sold as hardware, software subscription, or SaaS subscription. | character varying(30) | Offer Management |
| business_entity | Business Entity | Internal business unit or portfolio responsible for the product. | character varying(30) | Organizational Reporting |

---

# Table: QuoteToBooking.dim_sales_rep

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_sales_rep |
| Business Term | Sales Representative |
| Business Definition | Stores information about sales personnel responsible for managing customer relationships and booking transactions. |
| Business Category | Sales Performance Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| sales_rep_key | Sales Representative Key | Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. | integer | Technical Identifier |
| rep_id | Sales Representative ID | Business identifier assigned to the sales representative. | character varying(20) | Sales Performance Management |
| rep_name | Sales Representative Name | Full name of the sales representative associated with the booking. | character varying(60) | Sales Performance Management |
| sales_role | Sales Role | Job role or account responsibility of the sales representative. | character varying(40) | Sales Organization |
| sales_team | Sales Team | Team or organizational unit to which the sales representative belongs. | character varying(40) | Sales Organization |
| segment_covered | Covered Segment | Customer segment for which the sales representative is responsible. | character varying(30) | Sales Coverage |

---

# Table: QuoteToBooking.fact_bookings

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.fact_bookings |
| Business Term | Booking Transaction |
| Business Definition | Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions. |
| Business Category | Sales Bookings |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| booking_id | Booking ID | Unique identifier for an individual booking transaction record. | integer | Sales Bookings |
| order_number | Order Number | Business order number associated with the booking transaction. | character varying(20) | Order Management |
| order_line_number | Order Line Number | Line item number within the order associated with the booking. | integer | Order Management |
| date_key | Booking Date Key | Foreign key linking the booking transaction to the reporting date dimension. | integer | Time Management |
| customer_key | Customer Key | Foreign key linking the booking transaction to the customer dimension. | integer | Customer Management |
| product_key | Product Key | Foreign key linking the booking transaction to the product dimension. | integer | Product Management |
| partner_key | Partner Key | Foreign key linking the booking transaction to the partner dimension. | integer | Partner Management |
| geography_key | Geography Key | Foreign key linking the booking transaction to the geography dimension. | integer | Geographic Analysis |
| sales_rep_key | Sales Representative Key | Foreign key linking the booking transaction to the sales representative dimension. | integer | Sales Performance Management |
| contract_key | Contract Key | Foreign key linking the booking transaction to the contract dimension. | integer | Contract Management |
| booking_type | Booking Type | Indicates whether the booking is a new sale or a renewal. | character varying(15) | Sales Bookings |
| is_renewal | Renewal Indicator | Indicates whether the booking transaction is classified as a renewal. | integer | Renewal Management |
| quantity | Quantity Sold | Number of units, licenses, or subscriptions included in the booking transaction. | integer | Sales Measures |
| unit_list_price_usd | Unit List Price USD | Standard list price per unit in U.S. dollars before discounts are applied. | numeric | Pricing |
| discount_pct | Discount Percentage | Percentage discount applied to the list price for the booking transaction. | numeric | Pricing |
| booking_amount_usd | Booking Amount USD | Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments. | numeric | Revenue Measures |
| acv_usd | Annual Contract Value USD | Annualized value of the contract associated with the booking in U.S. dollars. | numeric | Revenue Measures |
| tcv_usd | Total Contract Value USD | Total value of the full contract associated with the booking in U.S. dollars. | numeric | Revenue Measures |
