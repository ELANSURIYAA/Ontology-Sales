# Business Glossary Data Dictionary

## Business Domain Context
Business domain context file was not available at `Inputs/Sales.txt`, so the glossary below is inferred from the schema metadata, table structures, relationships, and profiling results. The dataset represents a sales and quote-to-booking analytical model with supporting operational tables for client migration and agent execution logging.

# Table: clarity.client

## Table Information

| Field | Value |
|--------|-------|
| Table Name | clarity.client |
| Business Term | Client |
| Business Definition | Stores client and financial institution migration details, contact information, routing data, activation options, network participation, and migration planning attributes. |
| Business Category | Client Migration |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| client_id | Client Identifier | Unique identifier for the client record. | bigint | Client Migration |
| migration_date | Migration Date | Date on which the client is scheduled or completed for migration. | date | Client Migration |
| financial_institution_name | Financial Institution Name | Name of the bank, credit union, or financial institution associated with the client. | character varying(255) | Organization |
| entity_id | Entity Identifier | Identifier for the business entity associated with the client. | bigint | Organization |
| cardcount | Card Count | Number of cards associated with the client portfolio. | integer | Portfolio Metrics |
| vru_activation_options | VRU Activation Options | Available activation channels such as IVR, SMS, or mobile app for the client. | character varying(255) | Service Configuration |
| fi_id | Financial Institution Identifier | Internal identifier for the financial institution. | bigint | Organization |
| aims_id | AIMS Identifier | Identifier from the AIMS source or reference system. | bigint | Reference Data |
| ig_league_name | IG League Name | League or grouping assigned to the client within the IG classification structure. | character varying(255) | Segmentation |
| arb | Annual Revenue Base | Revenue-related metric associated with the client account. | numeric(15,2) | Financial Metrics |
| routing_id | Routing Identifier | Banking or payment routing identifier associated with the client. | character varying(50) | Banking Reference |
| city | City | City of the client or financial institution address. | character varying(100) | Location |
| state_name | State Name | State or province of the client or financial institution address. | character varying(100) | Location |
| fi_primary_contact_name | Financial Institution Primary Contact Name | Name of the primary contact at the financial institution. | character varying(255) | Contact Information |
| fi_primary_contact_phone | Financial Institution Primary Contact Phone | Phone number of the primary contact at the financial institution. | character varying(50) | Contact Information |
| fraudcontactgroup_email | Fraud Contact Group Email | Email address for the fraud contact group associated with the client. | character varying(255) | Contact Information |
| address | Address | Street address of the client or financial institution. | character varying(500) | Location |
| zip | ZIP Code | Postal code for the client or financial institution address. | character varying(20) | Location |
| fi_primary_contact_email | Financial Institution Primary Contact Email | Email address of the primary financial institution contact. | character varying(255) | Contact Information |
| current_pseudorouting | Current Pseudo Routing | Current pseudo-routing code assigned to the client. | character varying(50) | Banking Reference |
| issuing_networks | Issuing Networks | Payment card issuing networks used by the client. | character varying(255) | Network Participation |
| aquiring_networks | Acquiring Networks | Payment acquiring networks used by the client. | character varying(255) | Network Participation |
| vau_segment_id | VAU Segment Identifier | Identifier for the VAU segment associated with the client. | bigint | Segmentation |
| migration_wave | Migration Wave | Planned migration wave number for the client. | integer | Migration Planning |

---

# Table: logging.combined_agent_details

## Table Information

| Field | Value |
|--------|-------|
| Table Name | logging.combined_agent_details |
| Business Term | Combined Agent Execution Detail |
| Business Definition | Stores combined processing, ticketing, GitHub attachment, status, and diagnostic log details for automated agent executions. |
| Business Category | Process Logging |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| id | Execution Record Identifier | Unique identifier for the combined agent execution record. | bigint | Process Logging |
| project_key | Project Key | Key of the project associated with the ticket or workflow. | character varying(50) | Ticketing |
| ticket_key | Ticket Key | Human-readable issue or ticket key created or referenced by the process. | character varying(100) | Ticketing |
| ticket_id | Ticket Identifier | System identifier of the issue or ticket. | character varying(100) | Ticketing |
| ticket_url | Ticket URL | Web link to the issue or ticket record. | text | Ticketing |
| github_owner | GitHub Owner | GitHub account or organization that owns the repository. | character varying(255) | Source Control |
| github_repository | GitHub Repository | Name of the GitHub repository involved in the process. | character varying(255) | Source Control |
| github_branch | GitHub Branch | Branch in the GitHub repository used during processing. | character varying(255) | Source Control |
| github_file_path | GitHub File Path | Repository file path for the attachment or processed file. | text | Source Control |
| attachment_id | Attachment Identifier | Identifier of the file attachment associated with the ticket. | character varying(100) | Attachment Management |
| attachment_name | Attachment Name | Name of the attached file. | text | Attachment Management |
| attachment_status | Attachment Status | Outcome status of the attachment step. | character varying(50) | Process Status |
| status | Execution Status | Overall outcome status of the combined agent process. | character varying(50) | Process Status |
| error_message | Error Message | Error message captured during execution, if any. | text | Error Handling |
| diagnostic_logs | Diagnostic Logs | Structured diagnostic or audit messages recorded during execution. | jsonb | Audit Logging |
| created_at | Created Timestamp | Timestamp when the execution record was created. | timestamp without time zone | Audit Logging |

---

# Table: quotetobooking.dim_contract

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_contract |
| Business Term | Contract |
| Business Definition | Stores contract attributes used to classify bookings by agreement type, term, renewal behavior, and coverage level. |
| Business Category | Sales Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| contract_key | Contract Key | Surrogate key that uniquely identifies a contract record. | integer | Sales Dimension |
| contract_type | Contract Type | Type of contract or agreement associated with the booking. | character varying(40) | Contract Management |
| term_months | Contract Term Months | Length of the contract term in months. | integer | Contract Management |
| auto_renew_flag | Auto Renew Flag | Indicates whether the contract renews automatically. | character(1) | Contract Management |
| coverage_level | Coverage Level | Service or support coverage level included in the contract. | character varying(20) | Support Coverage |

---

# Table: quotetobooking.dim_customer

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_customer |
| Business Term | Customer |
| Business Definition | Stores customer master attributes used to analyze bookings by account, segment, industry, tier, and headquarters location. |
| Business Category | Sales Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| customer_key | Customer Key | Surrogate key that uniquely identifies a customer record. | integer | Sales Dimension |
| customer_id | Customer Identifier | Business identifier assigned to the customer account. | character varying(20) | Customer Master |
| customer_name | Customer Name | Name of the customer account or organization. | character varying(80) | Customer Master |
| segment | Customer Segment | Market segment to which the customer belongs, such as enterprise or service provider. | character varying(30) | Customer Segmentation |
| industry | Industry | Industry classification for the customer account. | character varying(40) | Customer Segmentation |
| account_tier | Account Tier | Strategic importance or tier assigned to the customer account. | character varying(20) | Customer Segmentation |
| hq_country | Headquarters Country | Country where the customer's headquarters is located. | character varying(40) | Geography |
| hq_region | Headquarters Region | Global region where the customer's headquarters is located. | character varying(20) | Geography |

---

# Table: quotetobooking.dim_date

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_date |
| Business Term | Date |
| Business Definition | Stores calendar and fiscal date attributes used to analyze bookings over time. |
| Business Category | Time Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| date_key | Date Key | Numeric surrogate key representing a calendar date. | integer | Time Dimension |
| full_date | Full Date | Actual calendar date represented by the date record. | date | Time Dimension |
| month_name | Month Name | Name of the calendar month. | character varying(12) | Calendar |
| calendar_year | Calendar Year | Four-digit calendar year. | integer | Calendar |
| fiscal_year | Fiscal Year | Fiscal year label used for business reporting. | character varying(6) | Fiscal Calendar |
| fiscal_quarter | Fiscal Quarter | Fiscal quarter label used for reporting and analysis. | character varying(10) | Fiscal Calendar |
| fiscal_period_seq | Fiscal Period Sequence | Sequential fiscal period number within the reporting cycle. | integer | Fiscal Calendar |

---

# Table: quotetobooking.dim_geography

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_geography |
| Business Term | Geography |
| Business Definition | Stores geographic attributes used to analyze bookings by region, theater, and country. |
| Business Category | Sales Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| geography_key | Geography Key | Surrogate key that uniquely identifies a geography record. | integer | Sales Dimension |
| region | Region | High-level geographic region used for reporting. | character varying(20) | Geography |
| theater | Theater | Sales theater or subregion within the broader region. | character varying(30) | Geography |
| country | Country | Country associated with the geography record. | character varying(40) | Geography |

---

# Table: quotetobooking.dim_partner

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_partner |
| Business Term | Partner |
| Business Definition | Stores partner attributes used to analyze bookings by channel partner, partner type, tier, and route to market. |
| Business Category | Channel Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| partner_key | Partner Key | Surrogate key that uniquely identifies a partner record. | integer | Channel Dimension |
| partner_id | Partner Identifier | Business identifier assigned to the partner. | character varying(20) | Partner Master |
| partner_name | Partner Name | Name of the partner organization. | character varying(60) | Partner Master |
| partner_type | Partner Type | Classification of the partner, such as reseller, distributor, or integrator. | character varying(30) | Partner Classification |
| partner_tier | Partner Tier | Program tier or status assigned to the partner. | character varying(30) | Partner Classification |
| route_to_market | Route to Market | Sales motion or channel route through which the offering is sold. | character varying(20) | Channel Strategy |

---

# Table: quotetobooking.dim_product

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_product |
| Business Term | Product |
| Business Definition | Stores product master attributes used to analyze bookings by product, family, technology domain, offer type, and business entity. |
| Business Category | Product Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| product_key | Product Key | Surrogate key that uniquely identifies a product record. | integer | Product Dimension |
| product_id | Product Identifier | Business identifier or SKU for the product. | character varying(30) | Product Master |
| product_name | Product Name | Descriptive name of the product or offer. | character varying(80) | Product Master |
| product_family | Product Family | Family grouping to which the product belongs. | character varying(30) | Product Classification |
| technology_domain | Technology Domain | Technology area or solution domain of the product. | character varying(40) | Product Classification |
| offer_type | Offer Type | Type of commercial offer, such as hardware or subscription. | character varying(30) | Commercial Offer |
| business_entity | Business Entity | Internal business entity aligned to the product. | character varying(30) | Organizational Alignment |

---

# Table: quotetobooking.dim_sales_rep

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.dim_sales_rep |
| Business Term | Sales Representative |
| Business Definition | Stores sales representative attributes used to analyze bookings by seller, role, team, and covered segment. |
| Business Category | Sales Dimension |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| sales_rep_key | Sales Representative Key | Surrogate key that uniquely identifies a sales representative record. | integer | Sales Dimension |
| rep_id | Sales Representative Identifier | Business identifier assigned to the sales representative. | character varying(20) | Sales Organization |
| rep_name | Sales Representative Name | Full name of the sales representative. | character varying(60) | Sales Organization |
| sales_role | Sales Role | Role performed by the sales representative. | character varying(40) | Sales Organization |
| sales_team | Sales Team | Team or organization to which the sales representative belongs. | character varying(40) | Sales Organization |
| segment_covered | Covered Segment | Customer segment covered by the sales representative. | character varying(30) | Sales Coverage |

---

# Table: quotetobooking.fact_bookings

## Table Information

| Field | Value |
|--------|-------|
| Table Name | quotetobooking.fact_bookings |
| Business Term | Booking |
| Business Definition | Stores sales booking transactions and measures, linked to customer, product, partner, geography, sales representative, contract, and date dimensions for quote-to-booking analysis. |
| Business Category | Sales Fact |

### Columns

| Column Name | Business Term | Business Definition | Data Type | Business Category |
|-------------|---------------|---------------------|-----------|-------------------|
| booking_id | Booking Identifier | Unique identifier for the booking transaction. | integer | Sales Fact |
| order_number | Order Number | Sales order number associated with the booking. | character varying(20) | Order Management |
| order_line_number | Order Line Number | Line number within the sales order. | integer | Order Management |
| date_key | Booking Date Key | Reference to the date dimension for the booking. | integer | Time Dimension |
| customer_key | Customer Key | Reference to the customer dimension for the booking. | integer | Customer Dimension |
| product_key | Product Key | Reference to the product dimension for the booking. | integer | Product Dimension |
| partner_key | Partner Key | Reference to the partner dimension for the booking. | integer | Channel Dimension |
| geography_key | Geography Key | Reference to the geography dimension for the booking. | integer | Geography Dimension |
| sales_rep_key | Sales Representative Key | Reference to the sales representative dimension for the booking. | integer | Sales Dimension |
| contract_key | Contract Key | Reference to the contract dimension for the booking. | integer | Contract Dimension |
| booking_type | Booking Type | Indicates whether the booking is new business or a renewal. | character varying(15) | Sales Classification |
| is_renewal | Renewal Indicator | Indicates whether the booking is a renewal transaction. | integer | Sales Classification |
| quantity | Quantity | Number of units included in the booking transaction. | integer | Sales Measures |
| unit_list_price_usd | Unit List Price USD | Standard list price per unit in US dollars before discount. | numeric(12,2) | Pricing |
| discount_pct | Discount Percentage | Discount percentage applied to the booking. | numeric(5,2) | Pricing |
| booking_amount_usd | Booking Amount USD | Total booked revenue amount in US dollars after pricing adjustments. | numeric(14,2) | Revenue Metrics |
| acv_usd | Annual Contract Value USD | Annualized contract value of the booking in US dollars. | numeric(14,2) | Revenue Metrics |
| tcv_usd | Total Contract Value USD | Total contract value of the booking in US dollars. | numeric(14,2) | Revenue Metrics |
