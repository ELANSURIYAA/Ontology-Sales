## Domains

| Domain ID | Domain Name | Description |
| --- | --- | --- |
| DOM001 | Sales Transactions | Completed customer booking transactions and associated sales performance measures across orders, renewals, quantities, pricing, and revenue values. |
| DOM002 | Customer Management | Customer master data used to analyze bookings by customer identity, segment, industry, account tier, and headquarters location. |
| DOM003 | Product Management | Product and offer master data used to analyze bookings by product identity, family, technology domain, offer type, and business entity. |
| DOM004 | Partner Management | Channel partner master data used to analyze bookings by partner identity, type, tier, and route to market. |
| DOM005 | Geography | Geographic master data used to analyze bookings by region, theater, and country. |
| DOM006 | Sales Organization | Sales representative and organizational attributes used to analyze bookings by seller, role, team, and covered segment. |
| DOM007 | Contract Management | Contract and service agreement attributes used to classify bookings by contract type, term, renewal behavior, and coverage level. |
| DOM008 | Time Management | Calendar and fiscal time attributes used to analyze bookings across dates, months, years, quarters, and fiscal periods. |
| DOM009 | Pricing | Pricing attributes used to analyze unit list price and discount characteristics of booked transactions. |
| DOM010 | Revenue Metrics | Financial value attributes used to analyze booked revenue, annual contract value, and total contract value. |

## Entities

| Entity ID | Domain ID | Business Name | Technical Table Name | Description | Business Keys |
| --- | --- | --- | --- | --- | --- |
| ENT001 | DOM007 | Contract Dimension | quotetobooking.dim_contract | Stores contract and service agreement attributes used to classify bookings by contract type, term, renewal behavior, and coverage level. | Contract Key |
| ENT002 | DOM002 | Customer Dimension | quotetobooking.dim_customer | Stores descriptive customer attributes used to analyze bookings by customer identity, segment, industry, account tier, and headquarters location. | Customer Key; Customer ID |
| ENT003 | DOM008 | Date Dimension | quotetobooking.dim_date | Stores calendar and fiscal date attributes used to analyze bookings across time periods, fiscal years, quarters, and months. | Date Key; Full Date |
| ENT004 | DOM005 | Geography Dimension | quotetobooking.dim_geography | Stores geographic attributes used to analyze bookings by region, theater, and country. | Geography Key |
| ENT005 | DOM004 | Partner Dimension | quotetobooking.dim_partner | Stores channel partner attributes used to analyze bookings by partner identity, partner type, partner tier, and route to market. | Partner Key; Partner ID |
| ENT006 | DOM003 | Product Dimension | quotetobooking.dim_product | Stores product and offer attributes used to analyze bookings by product identity, family, technology domain, offer type, and business entity. | Product Key; Product ID |
| ENT007 | DOM006 | Sales Representative Dimension | quotetobooking.dim_sales_rep | Stores sales representative attributes used to analyze bookings by sales person, role, team, and market segment coverage. | Sales Representative Key; Sales Representative ID |
| ENT008 | DOM001 | Booking Fact | quotetobooking.fact_bookings | Stores individual booking transactions and their financial measures for analyzing sales performance across customers, products, partners, geographies, contracts, sales representatives, and time. | Booking ID; Order Number; Order Line Number |

## Attributes

| Attribute ID | Entity ID | Business Attribute | Technical Column | Data Type | Nullable | Primary Key | Foreign Key | Description |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ATT001 | ENT001 | Contract Key | contract_key | integer | No | Yes | No | Surrogate key that uniquely identifies a contract record in the contract dimension. |
| ATT002 | ENT001 | Contract Type | contract_type | character varying(40) | Yes | No | No | Type of commercial agreement associated with the booking, such as Enterprise Agreement, SaaS Subscription, or support contract. |
| ATT003 | ENT001 | Contract Term Months | term_months | integer | Yes | No | No | Number of months covered by the contract or service agreement. |
| ATT004 | ENT001 | Auto Renew Flag | auto_renew_flag | character(1) | Yes | No | No | Indicator showing whether the contract is configured to renew automatically. |
| ATT005 | ENT001 | Coverage Level | coverage_level | character varying(20) | Yes | No | No | Service or support coverage level provided under the contract. |
| ATT006 | ENT002 | Customer Key | customer_key | integer | No | Yes | No | Surrogate key that uniquely identifies a customer record in the customer dimension. |
| ATT007 | ENT002 | Customer ID | customer_id | character varying(20) | No | No | No | Business identifier assigned to the customer account. |
| ATT008 | ENT002 | Customer Name | customer_name | character varying(80) | Yes | No | No | Name of the customer organization that placed the order. |
| ATT009 | ENT002 | Customer Segment | segment | character varying(30) | Yes | No | No | Market segment to which the customer belongs, such as Enterprise, Service Provider, or Public Sector. |
| ATT010 | ENT002 | Industry | industry | character varying(40) | Yes | No | No | Industry classification of the customer organization. |
| ATT011 | ENT002 | Account Tier | account_tier | character varying(20) | Yes | No | No | Strategic importance or tier assigned to the customer account. |
| ATT012 | ENT002 | Headquarters Country | hq_country | character varying(40) | Yes | No | No | Country where the customer organization's headquarters is located. |
| ATT013 | ENT002 | Headquarters Region | hq_region | character varying(20) | Yes | No | No | Global region where the customer headquarters is located. |
| ATT014 | ENT003 | Date Key | date_key | integer | No | Yes | No | Numeric date key representing a specific calendar date. |
| ATT015 | ENT003 | Full Date | full_date | date | No | No | No | Actual calendar date represented by the date record. |
| ATT016 | ENT003 | Month Name | month_name | character varying(12) | Yes | No | No | Name of the calendar month for the date. |
| ATT017 | ENT003 | Calendar Year | calendar_year | integer | Yes | No | No | Four-digit calendar year of the date. |
| ATT018 | ENT003 | Fiscal Year | fiscal_year | character varying(6) | Yes | No | No | Fiscal year used for business reporting and financial analysis. |
| ATT019 | ENT003 | Fiscal Quarter | fiscal_quarter | character varying(10) | Yes | No | No | Fiscal quarter associated with the date for reporting purposes. |
| ATT020 | ENT003 | Fiscal Period Sequence | fiscal_period_seq | integer | Yes | No | No | Sequential number representing the fiscal period order in the reporting calendar. |
| ATT021 | ENT004 | Geography Key | geography_key | integer | No | Yes | No | Surrogate key that uniquely identifies a geography record in the geography dimension. |
| ATT022 | ENT004 | Region | region | character varying(20) | Yes | No | No | Broad global sales region associated with the booking, such as Americas, EMEA, or APJC. |
| ATT023 | ENT004 | Theater | theater | character varying(30) | Yes | No | No | Sales theater or sub-region used for operational reporting within a region. |
| ATT024 | ENT004 | Country | country | character varying(40) | Yes | No | No | Country associated with the geography record. |
| ATT025 | ENT005 | Partner Key | partner_key | integer | No | Yes | No | Surrogate key that uniquely identifies a partner record in the partner dimension. |
| ATT026 | ENT005 | Partner ID | partner_id | character varying(20) | No | No | No | Business identifier assigned to the partner organization. |
| ATT027 | ENT005 | Partner Name | partner_name | character varying(60) | Yes | No | No | Name of the distributor, reseller, integrator, or direct channel partner involved in the booking. |
| ATT028 | ENT005 | Partner Type | partner_type | character varying(30) | Yes | No | No | Classification of the partner, such as distributor, value-added reseller, systems integrator, or direct. |
| ATT029 | ENT005 | Partner Tier | partner_tier | character varying(30) | Yes | No | No | Tier or certification level assigned to the partner in the channel program. |
| ATT030 | ENT005 | Route to Market | route_to_market | character varying(20) | Yes | No | No | Sales route through which the booking was transacted, such as direct, reseller, or two-tier. |
| ATT031 | ENT006 | Product Key | product_key | integer | No | Yes | No | Surrogate key that uniquely identifies a product record in the product dimension. |
| ATT032 | ENT006 | Product ID | product_id | character varying(30) | No | No | No | Business identifier or SKU assigned to the product or subscription offer. |
| ATT033 | ENT006 | Product Name | product_name | character varying(80) | Yes | No | No | Descriptive name of the product, service, or subscription offer. |
| ATT034 | ENT006 | Product Family | product_family | character varying(30) | Yes | No | No | Higher-level grouping of related products within the portfolio. |
| ATT035 | ENT006 | Technology Domain | technology_domain | character varying(40) | Yes | No | No | Technology area to which the product belongs, such as networking, security, or collaboration. |
| ATT036 | ENT006 | Offer Type | offer_type | character varying(30) | Yes | No | No | Commercial offer classification, such as hardware, SaaS subscription, or software subscription. |
| ATT037 | ENT006 | Business Entity | business_entity | character varying(30) | Yes | No | No | Internal business portfolio or organizational entity responsible for the product. |
| ATT038 | ENT007 | Sales Representative Key | sales_rep_key | integer | No | Yes | No | Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. |
| ATT039 | ENT007 | Sales Representative ID | rep_id | character varying(20) | No | No | No | Business identifier assigned to the sales representative. |
| ATT040 | ENT007 | Sales Representative Name | rep_name | character varying(60) | Yes | No | No | Full name of the sales representative managing the account or opportunity. |
| ATT041 | ENT007 | Sales Role | sales_role | character varying(40) | Yes | No | No | Job role or selling role performed by the sales representative. |
| ATT042 | ENT007 | Sales Team | sales_team | character varying(40) | Yes | No | No | Sales team or organization to which the representative belongs. |
| ATT043 | ENT007 | Segment Covered | segment_covered | character varying(30) | Yes | No | No | Customer segment primarily covered by the sales representative. |
| ATT044 | ENT008 | Booking ID | booking_id | integer | No | Yes | No | Unique identifier for an individual booking transaction. |
| ATT045 | ENT008 | Order Number | order_number | character varying(20) | Yes | No | No | Sales order number associated with the booking transaction. |
| ATT046 | ENT008 | Order Line Number | order_line_number | integer | Yes | No | No | Line number within the sales order that identifies the specific booked item. |
| ATT047 | ENT008 | Date Key | date_key | integer | Yes | No | Yes | Reference to the date dimension indicating when the booking was recorded. |
| ATT048 | ENT008 | Customer Key | customer_key | integer | Yes | No | Yes | Reference to the customer associated with the booking. |
| ATT049 | ENT008 | Product Key | product_key | integer | Yes | No | Yes | Reference to the product or offer included in the booking. |
| ATT050 | ENT008 | Partner Key | partner_key | integer | Yes | No | Yes | Reference to the partner involved in fulfilling or transacting the booking. |
| ATT051 | ENT008 | Geography Key | geography_key | integer | Yes | No | Yes | Reference to the geography associated with the booking. |
| ATT052 | ENT008 | Sales Representative Key | sales_rep_key | integer | Yes | No | Yes | Reference to the sales representative responsible for the booking. |
| ATT053 | ENT008 | Contract Key | contract_key | integer | Yes | No | Yes | Reference to the contract or commercial agreement associated with the booking. |
| ATT054 | ENT008 | Booking Type | booking_type | character varying(15) | Yes | No | No | Classification of the booking event, such as new business or renewal. |
| ATT055 | ENT008 | Renewal Indicator | is_renewal | integer | Yes | No | No | Indicator showing whether the booking represents a renewal transaction. |
| ATT056 | ENT008 | Quantity Sold | quantity | integer | Yes | No | No | Number of units, licenses, or subscriptions booked in the transaction. |
| ATT057 | ENT008 | Unit List Price USD | unit_list_price_usd | numeric(12,2) | Yes | No | No | Standard list price per unit in U.S. dollars before discounts. |
| ATT058 | ENT008 | Discount Percentage | discount_pct | numeric(5,2) | Yes | No | No | Discount applied to the list price for the booking line. |
| ATT059 | ENT008 | Booking Amount USD | booking_amount_usd | numeric(14,2) | Yes | No | No | Total booked revenue amount in U.S. dollars for the transaction. |
| ATT060 | ENT008 | Annual Contract Value USD | acv_usd | numeric(14,2) | Yes | No | No | Annualized contract value in U.S. dollars used for recurring revenue analysis. |
| ATT061 | ENT008 | Total Contract Value USD | tcv_usd | numeric(14,2) | Yes | No | No | Total contract value in U.S. dollars over the full contract term. |

## Measures

| Measure ID | Entity ID | Measure Name | Technical Column | Business Definition | Aggregation Type |
| --- | --- | --- | --- | --- | --- |
| MEA001 | ENT008 | Quantity Sold | quantity | Number of units, licenses, or subscriptions booked in the transaction. | Sum |
| MEA002 | ENT008 | Unit List Price USD | unit_list_price_usd | Standard list price per unit in U.S. dollars before discounts. | Average |
| MEA003 | ENT008 | Discount Percentage | discount_pct | Discount applied to the list price for the booking line. | Average |
| MEA004 | ENT008 | Booking Amount USD | booking_amount_usd | Total booked revenue amount in U.S. dollars for the transaction. | Sum |
| MEA005 | ENT008 | Annual Contract Value USD | acv_usd | Annualized contract value in U.S. dollars used for recurring revenue analysis. | Sum |
| MEA006 | ENT008 | Total Contract Value USD | tcv_usd | Total contract value in U.S. dollars over the full contract term. | Sum |

## Relationships

| Relationship ID | Parent Entity | Child Entity | Parent Attribute | Child Attribute | Relationship Type | Cardinality | Confidence Score |
| --- | --- | --- | --- | --- | --- | --- | --- |
| REL001 | Contract Dimension | Booking Fact | Contract Key | Contract Key | Foreign Key Relationship | One-to-Many | 1.00 |
| REL002 | Customer Dimension | Booking Fact | Customer Key | Customer Key | Foreign Key Relationship | One-to-Many | 1.00 |
| REL003 | Date Dimension | Booking Fact | Date Key | Date Key | Foreign Key Relationship | One-to-Many | 1.00 |
| REL004 | Geography Dimension | Booking Fact | Geography Key | Geography Key | Foreign Key Relationship | One-to-Many | 1.00 |
| REL005 | Partner Dimension | Booking Fact | Partner Key | Partner Key | Foreign Key Relationship | One-to-Many | 1.00 |
| REL006 | Product Dimension | Booking Fact | Product Key | Product Key | Foreign Key Relationship | One-to-Many | 1.00 |
| REL007 | Sales Representative Dimension | Booking Fact | Sales Representative Key | Sales Representative Key | Foreign Key Relationship | One-to-Many | 1.00 |

## Glossary Mapping

| Business Term | Business Definition | Technical Mapping | Entity | Attribute | Confidence Score |
| --- | --- | --- | --- | --- | --- |
| Contract Dimension | Stores contract and service agreement attributes used to classify bookings by contract type, term, renewal behavior, and coverage level. | quotetobooking.dim_contract | Contract Dimension |  | 1.00 |
| Contract Key | Surrogate key that uniquely identifies a contract record in the contract dimension. | quotetobooking.dim_contract.contract_key | Contract Dimension | Contract Key | 1.00 |
| Contract Type | Type of commercial agreement associated with the booking, such as Enterprise Agreement, SaaS Subscription, or support contract. | quotetobooking.dim_contract.contract_type | Contract Dimension | Contract Type | 1.00 |
| Contract Term Months | Number of months covered by the contract or service agreement. | quotetobooking.dim_contract.term_months | Contract Dimension | Contract Term Months | 1.00 |
| Auto Renew Flag | Indicator showing whether the contract is configured to renew automatically. | quotetobooking.dim_contract.auto_renew_flag | Contract Dimension | Auto Renew Flag | 1.00 |
| Coverage Level | Service or support coverage level provided under the contract. | quotetobooking.dim_contract.coverage_level | Contract Dimension | Coverage Level | 1.00 |
| Customer Dimension | Stores descriptive customer attributes used to analyze bookings by customer identity, segment, industry, account tier, and headquarters location. | quotetobooking.dim_customer | Customer Dimension |  | 1.00 |
| Customer Key | Surrogate key that uniquely identifies a customer record in the customer dimension. | quotetobooking.dim_customer.customer_key | Customer Dimension | Customer Key | 1.00 |
| Customer ID | Business identifier assigned to the customer account. | quotetobooking.dim_customer.customer_id | Customer Dimension | Customer ID | 1.00 |
| Customer Name | Name of the customer organization that placed the order. | quotetobooking.dim_customer.customer_name | Customer Dimension | Customer Name | 1.00 |
| Customer Segment | Market segment to which the customer belongs, such as Enterprise, Service Provider, or Public Sector. | quotetobooking.dim_customer.segment | Customer Dimension | Customer Segment | 1.00 |
| Industry | Industry classification of the customer organization. | quotetobooking.dim_customer.industry | Customer Dimension | Industry | 1.00 |
| Account Tier | Strategic importance or tier assigned to the customer account. | quotetobooking.dim_customer.account_tier | Customer Dimension | Account Tier | 1.00 |
| Headquarters Country | Country where the customer organization's headquarters is located. | quotetobooking.dim_customer.hq_country | Customer Dimension | Headquarters Country | 1.00 |
| Headquarters Region | Global region where the customer headquarters is located. | quotetobooking.dim_customer.hq_region | Customer Dimension | Headquarters Region | 1.00 |
| Date Dimension | Stores calendar and fiscal date attributes used to analyze bookings across time periods, fiscal years, quarters, and months. | quotetobooking.dim_date | Date Dimension |  | 1.00 |
| Date Key | Numeric surrogate key representing a specific calendar date. | quotetobooking.dim_date.date_key | Date Dimension | Date Key | 1.00 |
| Full Date | Actual calendar date represented by the date record. | quotetobooking.dim_date.full_date | Date Dimension | Full Date | 1.00 |
| Month Name | Name of the calendar month for the date. | quotetobooking.dim_date.month_name | Date Dimension | Month Name | 1.00 |
| Calendar Year | Four-digit calendar year of the date. | quotetobooking.dim_date.calendar_year | Date Dimension | Calendar Year | 1.00 |
| Fiscal Year | Fiscal year used for business reporting and financial analysis. | quotetobooking.dim_date.fiscal_year | Date Dimension | Fiscal Year | 1.00 |
| Fiscal Quarter | Fiscal quarter associated with the date for reporting purposes. | quotetobooking.dim_date.fiscal_quarter | Date Dimension | Fiscal Quarter | 1.00 |
| Fiscal Period Sequence | Sequential number representing the fiscal period order in the reporting calendar. | quotetobooking.dim_date.fiscal_period_seq | Date Dimension | Fiscal Period Sequence | 1.00 |
| Geography Dimension | Stores geographic attributes used to analyze bookings by region, theater, and country. | quotetobooking.dim_geography | Geography Dimension |  | 1.00 |
| Geography Key | Surrogate key that uniquely identifies a geography record in the geography dimension. | quotetobooking.dim_geography.geography_key | Geography Dimension | Geography Key | 1.00 |
| Region | Broad global sales region associated with the booking, such as Americas, EMEA, or APJC. | quotetobooking.dim_geography.region | Geography Dimension | Region | 1.00 |
| Theater | Sales theater or sub-region used for operational reporting within a region. | quotetobooking.dim_geography.theater | Geography Dimension | Theater | 1.00 |
| Country | Country associated with the geography record. | quotetobooking.dim_geography.country | Geography Dimension | Country | 1.00 |
| Partner Dimension | Stores channel partner attributes used to analyze bookings by partner identity, partner type, partner tier, and route to market. | quotetobooking.dim_partner | Partner Dimension |  | 1.00 |
| Partner Key | Surrogate key that uniquely identifies a partner record in the partner dimension. | quotetobooking.dim_partner.partner_key | Partner Dimension | Partner Key | 1.00 |
| Partner ID | Business identifier assigned to the partner organization. | quotetobooking.dim_partner.partner_id | Partner Dimension | Partner ID | 1.00 |
| Partner Name | Name of the distributor, reseller, integrator, or direct channel partner involved in the booking. | quotetobooking.dim_partner.partner_name | Partner Dimension | Partner Name | 1.00 |
| Partner Type | Classification of the partner, such as distributor, value-added reseller, systems integrator, or direct. | quotetobooking.dim_partner.partner_type | Partner Dimension | Partner Type | 1.00 |
| Partner Tier | Tier or certification level assigned to the partner in the channel program. | quotetobooking.dim_partner.partner_tier | Partner Dimension | Partner Tier | 1.00 |
| Route to Market | Sales route through which the booking was transacted, such as direct, reseller, or two-tier. | quotetobooking.dim_partner.route_to_market | Partner Dimension | Route to Market | 1.00 |
| Product Dimension | Stores product and offer attributes used to analyze bookings by product identity, family, technology domain, offer type, and business entity. | quotetobooking.dim_product | Product Dimension |  | 1.00 |
| Product Key | Surrogate key that uniquely identifies a product record in the product dimension. | quotetobooking.dim_product.product_key | Product Dimension | Product Key | 1.00 |
| Product ID | Business identifier or SKU assigned to the product or subscription offer. | quotetobooking.dim_product.product_id | Product Dimension | Product ID | 1.00 |
| Product Name | Descriptive name of the product, service, or subscription offer. | quotetobooking.dim_product.product_name | Product Dimension | Product Name | 1.00 |
| Product Family | Higher-level grouping of related products within the portfolio. | quotetobooking.dim_product.product_family | Product Dimension | Product Family | 1.00 |
| Technology Domain | Technology area to which the product belongs, such as networking, security, or collaboration. | quotetobooking.dim_product.technology_domain | Product Dimension | Technology Domain | 1.00 |
| Offer Type | Commercial offer classification, such as hardware, SaaS subscription, or software subscription. | quotetobooking.dim_product.offer_type | Product Dimension | Offer Type | 1.00 |
| Business Entity | Internal business portfolio or organizational entity responsible for the product. | quotetobooking.dim_product.business_entity | Product Dimension | Business Entity | 1.00 |
| Sales Representative Dimension | Stores sales representative attributes used to analyze bookings by sales person, role, team, and market segment coverage. | quotetobooking.dim_sales_rep | Sales Representative Dimension |  | 1.00 |
| Sales Representative Key | Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. | quotetobooking.dim_sales_rep.sales_rep_key | Sales Representative Dimension | Sales Representative Key | 1.00 |
| Sales Representative ID | Business identifier assigned to the sales representative. | quotetobooking.dim_sales_rep.rep_id | Sales Representative Dimension | Sales Representative ID | 1.00 |
| Sales Representative Name | Full name of the sales representative managing the account or opportunity. | quotetobooking.dim_sales_rep.rep_name | Sales Representative Dimension | Sales Representative Name | 1.00 |
| Sales Role | Job role or selling role performed by the sales representative. | quotetobooking.dim_sales_rep.sales_role | Sales Representative Dimension | Sales Role | 1.00 |
| Sales Team | Sales team or organization to which the representative belongs. | quotetobooking.dim_sales_rep.sales_team | Sales Representative Dimension | Sales Team | 1.00 |
| Segment Covered | Customer segment primarily covered by the sales representative. | quotetobooking.dim_sales_rep.segment_covered | Sales Representative Dimension | Segment Covered | 1.00 |
| Booking Fact | Stores individual booking transactions and their financial measures for analyzing sales performance across customers, products, partners, geographies, contracts, sales representatives, and time. | quotetobooking.fact_bookings | Booking Fact |  | 1.00 |
| Booking ID | Unique identifier for an individual booking transaction. | quotetobooking.fact_bookings.booking_id | Booking Fact | Booking ID | 1.00 |
| Order Number | Sales order number associated with the booking transaction. | quotetobooking.fact_bookings.order_number | Booking Fact | Order Number | 1.00 |
| Order Line Number | Line number within the sales order that identifies the specific booked item. | quotetobooking.fact_bookings.order_line_number | Booking Fact | Order Line Number | 1.00 |
| Booking Type | Classification of the booking event, such as new business or renewal. | quotetobooking.fact_bookings.booking_type | Booking Fact | Booking Type | 1.00 |
| Renewal Indicator | Indicator showing whether the booking represents a renewal transaction. | quotetobooking.fact_bookings.is_renewal | Booking Fact | Renewal Indicator | 1.00 |
| Quantity Sold | Number of units, licenses, or subscriptions booked in the transaction. | quotetobooking.fact_bookings.quantity | Booking Fact | Quantity Sold | 1.00 |
| Unit List Price USD | Standard list price per unit in U.S. dollars before discounts. | quotetobooking.fact_bookings.unit_list_price_usd | Booking Fact | Unit List Price USD | 1.00 |
| Discount Percentage | Discount applied to the list price for the booking line. | quotetobooking.fact_bookings.discount_pct | Booking Fact | Discount Percentage | 1.00 |
| Booking Amount USD | Total booked revenue amount in U.S. dollars for the transaction. | quotetobooking.fact_bookings.booking_amount_usd | Booking Fact | Booking Amount USD | 1.00 |
| Annual Contract Value USD | Annualized contract value in U.S. dollars used for recurring revenue analysis. | quotetobooking.fact_bookings.acv_usd | Booking Fact | Annual Contract Value USD | 1.00 |
| Total Contract Value USD | Total contract value in U.S. dollars over the full contract term. | quotetobooking.fact_bookings.tcv_usd | Booking Fact | Total Contract Value USD | 1.00 |
| Customer Key | Reference to the customer associated with the booking. | quotetobooking.fact_bookings.customer_key | Booking Fact | Customer Key | 1.00 |
| Product Key | Reference to the product or offer included in the booking. | quotetobooking.fact_bookings.product_key | Booking Fact | Product Key | 1.00 |
| Partner Key | Reference to the partner involved in fulfilling or transacting the booking. | quotetobooking.fact_bookings.partner_key | Booking Fact | Partner Key | 1.00 |
| Geography Key | Reference to the geography associated with the booking. | quotetobooking.fact_bookings.geography_key | Booking Fact | Geography Key | 1.00 |
| Sales Representative Key | Reference to the sales representative responsible for the booking. | quotetobooking.fact_bookings.sales_rep_key | Booking Fact | Sales Representative Key | 1.00 |
| Contract Key | Reference to the contract or commercial agreement associated with the booking. | quotetobooking.fact_bookings.contract_key | Booking Fact | Contract Key | 1.00 |
| Date Key | Reference to the date dimension indicating when the booking was recorded. | quotetobooking.fact_bookings.date_key | Booking Fact | Date Key | 1.00 |