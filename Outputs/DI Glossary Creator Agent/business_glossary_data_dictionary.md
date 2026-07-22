# Business Domain Context

**Domain Name:** Sales Bookings and Revenue Analytics

This domain supports analysis of completed sales bookings for enterprise products and subscription services across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods. The model follows a star schema where booking transactions are measured in the fact table and descriptive business context is provided through dimension tables.

# Table: QuoteToBooking.dim_contract

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_contract |
| Business Term | Contract |
| Business Definition | Stores the contractual attributes associated with a booking, including agreement type, duration, renewal behavior, and support or service coverage level. |
| Business Category | Contract Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| contract_key | Contract Key | Surrogate key that uniquely identifies a contract record in the contract dimension. | integer | Technical Identifier |
| contract_type | Contract Type | Indicates the type of commercial agreement or service contract associated with the booking, such as SaaS Subscription or Enterprise Agreement. | character varying | Contract Management |
| term_months | Contract Term Months | Specifies the duration of the contract in months. | integer | Contract Management |
| auto_renew_flag | Auto Renew Indicator | Indicates whether the contract is configured to renew automatically. | character | Renewal Management |
| coverage_level | Coverage Level | Describes the support, service, or entitlement coverage level provided under the contract. | character varying | Service Coverage |

---

# Table: QuoteToBooking.dim_customer

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_customer |
| Business Term | Customer |
| Business Definition | Stores customer master data used to analyze bookings by customer identity, market segment, industry, account tier, and headquarters location. |
| Business Category | Customer Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| customer_key | Customer Key | Surrogate key that uniquely identifies a customer record in the customer dimension. | integer | Technical Identifier |
| customer_id | Customer ID | Business identifier assigned to the customer account. | character varying | Customer Management |
| customer_name | Customer Name | Name of the customer organization associated with the booking. | character varying | Customer Management |
| segment | Customer Segment | Classifies the customer into a business segment such as Enterprise, Service Provider, or Public Sector. | character varying | Customer Segmentation |
| industry | Industry | Indicates the customer’s industry classification for business analysis. | character varying | Customer Segmentation |
| account_tier | Account Tier | Identifies the strategic importance or service tier of the customer account. | character varying | Account Management |
| hq_country | Headquarters Country | Country where the customer’s headquarters is located. | character varying | Customer Geography |
| hq_region | Headquarters Region | Region where the customer’s headquarters is located, such as Americas, EMEA, or APJC. | character varying | Customer Geography |

---

# Table: QuoteToBooking.dim_date

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_date |
| Business Term | Date |
| Business Definition | Stores calendar and fiscal date attributes used to analyze bookings over time and support period-based reporting. |
| Business Category | Time Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| date_key | Date Key | Surrogate or encoded key that uniquely identifies a date record in the date dimension. | integer | Technical Identifier |
| full_date | Full Date | Calendar date represented by the date dimension record. | date | Time Management |
| month_name | Month Name | Name of the calendar month for the date. | character varying | Calendar Reporting |
| calendar_year | Calendar Year | Four-digit calendar year associated with the date. | integer | Calendar Reporting |
| fiscal_year | Fiscal Year | Fiscal year used for business reporting and performance analysis. | character varying | Fiscal Reporting |
| fiscal_quarter | Fiscal Quarter | Fiscal quarter used for reporting and period-based business analysis. | character varying | Fiscal Reporting |
| fiscal_period_seq | Fiscal Period Sequence | Sequential number representing the order of the fiscal period in the reporting calendar. | integer | Fiscal Reporting |

---

# Table: QuoteToBooking.dim_geography

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_geography |
| Business Term | Geography |
| Business Definition | Stores geographic attributes used to analyze bookings across sales regions, theaters, and countries. |
| Business Category | Geographic Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| geography_key | Geography Key | Surrogate key that uniquely identifies a geography record in the geography dimension. | integer | Technical Identifier |
| region | Sales Region | High-level geographic region used for business reporting and sales analysis. | character varying | Geographic Management |
| theater | Sales Theater | Intermediate geographic sales area within a region used for operational reporting. | character varying | Geographic Management |
| country | Country | Country associated with the geography record for booking analysis. | character varying | Geographic Management |

---

# Table: QuoteToBooking.dim_partner

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_partner |
| Business Term | Partner |
| Business Definition | Stores partner master data used to analyze indirect and direct sales activity by partner identity, partner type, tier, and route to market. |
| Business Category | Partner Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| partner_key | Partner Key | Surrogate key that uniquely identifies a partner record in the partner dimension. | integer | Technical Identifier |
| partner_id | Partner ID | Business identifier assigned to the partner organization. | character varying | Partner Management |
| partner_name | Partner Name | Name of the partner organization involved in the sale or fulfillment process. | character varying | Partner Management |
| partner_type | Partner Type | Classifies the partner by business role, such as distributor, reseller, systems integrator, or direct. | character varying | Partner Classification |
| partner_tier | Partner Tier | Indicates the partner’s program tier or accreditation level. | character varying | Partner Classification |
| route_to_market | Route to Market | Describes the sales channel path through which the offering reaches the customer. | character varying | Channel Management |

---

# Table: QuoteToBooking.dim_product

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_product |
| Business Term | Product |
| Business Definition | Stores product master data used to analyze bookings by product identity, family, technology domain, offer type, and business entity. |
| Business Category | Product Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| product_key | Product Key | Surrogate key that uniquely identifies a product record in the product dimension. | integer | Technical Identifier |
| product_id | Product ID | Business identifier or SKU assigned to the product or offering. | character varying | Product Management |
| product_name | Product Name | Name of the product, solution, or subscription offering. | character varying | Product Management |
| product_family | Product Family | Groups related products into a common family for portfolio analysis. | character varying | Product Classification |
| technology_domain | Technology Domain | Identifies the technology area associated with the product, such as networking, security, or collaboration. | character varying | Product Classification |
| offer_type | Offer Type | Indicates whether the offering is hardware, software subscription, or SaaS subscription. | character varying | Offer Management |
| business_entity | Business Entity | Identifies the internal business unit or portfolio associated with the product. | character varying | Product Portfolio |

---

# Table: QuoteToBooking.dim_sales_rep

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.dim_sales_rep |
| Business Term | Sales Representative |
| Business Definition | Stores sales representative attributes used to analyze bookings by individual seller, role, team, and covered segment. |
| Business Category | Sales Force Management |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| sales_rep_key | Sales Representative Key | Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. | integer | Technical Identifier |
| rep_id | Sales Representative ID | Business identifier assigned to the sales representative. | character varying | Sales Force Management |
| rep_name | Sales Representative Name | Full name of the sales representative responsible for the customer relationship or sale. | character varying | Sales Force Management |
| sales_role | Sales Role | Job role or selling responsibility of the sales representative. | character varying | Sales Organization |
| sales_team | Sales Team | Team or organizational unit to which the sales representative belongs. | character varying | Sales Organization |
| segment_covered | Covered Segment | Customer segment for which the sales representative is responsible. | character varying | Sales Coverage |

---

# Table: QuoteToBooking.fact_bookings

## Table Information

| Field | Value |
|--------|-------|
| Table Name | QuoteToBooking.fact_bookings |
| Business Term | Booking Transaction |
| Business Definition | Stores individual completed sales booking transactions and their associated financial measures, linked to customer, product, partner, geography, sales representative, contract, and date dimensions. |
| Business Category | Sales Performance |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| booking_id | Booking ID | Unique identifier for the booking transaction record. | integer | Transaction Identifier |
| order_number | Order Number | Business order number associated with the booking transaction. | character varying | Order Management |
| order_line_number | Order Line Number | Line number within the order associated with the booking transaction. | integer | Order Management |
| date_key | Booking Date Key | Foreign key linking the booking transaction to the date dimension. | integer | Time Management |
| customer_key | Customer Key | Foreign key linking the booking transaction to the customer dimension. | integer | Customer Management |
| product_key | Product Key | Foreign key linking the booking transaction to the product dimension. | integer | Product Management |
| partner_key | Partner Key | Foreign key linking the booking transaction to the partner dimension. | integer | Partner Management |
| geography_key | Geography Key | Foreign key linking the booking transaction to the geography dimension. | integer | Geographic Management |
| sales_rep_key | Sales Representative Key | Foreign key linking the booking transaction to the sales representative dimension. | integer | Sales Force Management |
| contract_key | Contract Key | Foreign key linking the booking transaction to the contract dimension. | integer | Contract Management |
| booking_type | Booking Type | Indicates whether the booking is a new sale or a renewal. | character varying | Sales Classification |
| is_renewal | Renewal Indicator | Indicates whether the booking transaction represents a renewal event. | integer | Renewal Management |
| quantity | Quantity Sold | Number of units, licenses, or service quantities included in the booking. | integer | Sales Measures |
| unit_list_price_usd | Unit List Price USD | Standard list price per unit in U.S. dollars before discounts. | numeric | Pricing |
| discount_pct | Discount Percentage | Discount applied to the list price for the booking transaction. | numeric | Pricing |
| booking_amount_usd | Booking Amount USD | Total booked sales value recognized for the transaction in U.S. dollars. | numeric | Revenue Measures |
| acv_usd | Annual Contract Value USD | Annualized value of the contract associated with the booking in U.S. dollars. | numeric | Revenue Measures |
| tcv_usd | Total Contract Value USD | Total contract value associated with the booking in U.S. dollars over the contract term. | numeric | Revenue Measures |
