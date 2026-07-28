## Domains

| Domain ID | Domain Name | Description |
| --- | --- | --- |
| DOM001 | Sales Bookings and Revenue Analytics | This domain represents sales booking operations for enterprise networking, security, collaboration, observability, and software subscription products. It captures completed customer bookings and supports analysis of sales performance across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods. |

## Entities

| Entity ID | Domain ID | Business Name | Technical Table Name | Description | Business Keys |
| --- | --- | --- | --- | --- | --- |
| ENT001 | DOM001 | Contract | QuoteToBooking.dim_contract | Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level. | Contract Key |
| ENT002 | DOM001 | Customer | QuoteToBooking.dim_customer | Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location. | Customer ID |
| ENT003 | DOM001 | Date | QuoteToBooking.dim_date | Stores calendar and fiscal date attributes used to analyze bookings over time. | Date Key |
| ENT004 | DOM001 | Geography | QuoteToBooking.dim_geography | Stores geographic attributes used to analyze bookings by sales region, theater, and country. | Geography Key |
| ENT005 | DOM001 | Partner | QuoteToBooking.dim_partner | Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market. | Partner ID |
| ENT006 | DOM001 | Product | QuoteToBooking.dim_product | Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity. | Product ID |
| ENT007 | DOM001 | Sales Representative | QuoteToBooking.dim_sales_rep | Stores information about sales personnel responsible for managing customer relationships and booking transactions. | Sales Representative ID |
| ENT008 | DOM001 | Booking Transaction | QuoteToBooking.fact_bookings | Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions. | Booking ID; Order Number; Order Line Number |

## Attributes

| Attribute ID | Entity ID | Business Attribute | Technical Column | Data Type | Nullable | Primary Key | Foreign Key | Description |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ATTR001 | ENT001 | Contract Key | contract_key | integer | No | Yes | No | Surrogate key that uniquely identifies a contract record in the contract dimension. |
| ATTR002 | ENT001 | Contract Type | contract_type | character varying(40) | Yes | No | No | Describes the type of commercial agreement attached to the booking, such as SaaS subscription, Enterprise Agreement, or support contract. |
| ATTR003 | ENT001 | Contract Term Months | term_months | integer | Yes | No | No | Indicates the duration of the contract in months. |
| ATTR004 | ENT001 | Auto Renew Flag | auto_renew_flag | character(1) | Yes | No | No | Indicates whether the contract is set to renew automatically at the end of its term. |
| ATTR005 | ENT001 | Coverage Level | coverage_level | character varying(20) | Yes | No | No | Describes the level of service or support coverage provided under the contract. |
| ATTR006 | ENT002 | Customer Key | customer_key | integer | No | Yes | No | Surrogate key that uniquely identifies a customer record in the customer dimension. |
| ATTR007 | ENT002 | Customer ID | customer_id | character varying(20) | No | No | No | Business identifier assigned to the customer account. |
| ATTR008 | ENT002 | Customer Name | customer_name | character varying(80) | Yes | No | No | Official name of the customer organization that purchased products or services. |
| ATTR009 | ENT002 | Customer Segment | segment | character varying(30) | Yes | No | No | Classifies the customer into a business segment such as Enterprise, Service Provider, or Public Sector. |
| ATTR010 | ENT002 | Industry | industry | character varying(40) | Yes | No | No | Identifies the industry in which the customer operates. |
| ATTR011 | ENT002 | Account Tier | account_tier | character varying(20) | Yes | No | No | Indicates the strategic importance or service tier of the customer account. |
| ATTR012 | ENT002 | Headquarters Country | hq_country | character varying(40) | Yes | No | No | Country where the customer organization's headquarters is located. |
| ATTR013 | ENT002 | Headquarters Region | hq_region | character varying(20) | Yes | No | No | Global region where the customer organization's headquarters is located. |
| ATTR014 | ENT003 | Date Key | date_key | integer | No | Yes | No | Encoded key that uniquely identifies a reporting date in the date dimension. |
| ATTR015 | ENT003 | Full Date | full_date | date | No | No | No | Actual calendar date represented by the date record. |
| ATTR016 | ENT003 | Month Name | month_name | character varying(12) | Yes | No | No | Name of the calendar month for the date. |
| ATTR017 | ENT003 | Calendar Year | calendar_year | integer | Yes | No | No | Four-digit calendar year associated with the date. |
| ATTR018 | ENT003 | Fiscal Year | fiscal_year | character varying(6) | Yes | No | No | Fiscal year used by the business for financial and performance reporting. |
| ATTR019 | ENT003 | Fiscal Quarter | fiscal_quarter | character varying(10) | Yes | No | No | Fiscal quarter used by the business for periodic reporting and analysis. |
| ATTR020 | ENT003 | Fiscal Period Sequence | fiscal_period_seq | integer | Yes | No | No | Sequential number representing the fiscal reporting period in ordered time analysis. |
| ATTR021 | ENT004 | Geography Key | geography_key | integer | No | Yes | No | Surrogate key that uniquely identifies a geography record in the geography dimension. |
| ATTR022 | ENT004 | Sales Region | region | character varying(20) | Yes | No | No | High-level geographic region used for reporting and performance analysis. |
| ATTR023 | ENT004 | Sales Theater | theater | character varying(30) | Yes | No | No | Subregional sales area or theater used to organize market coverage and reporting. |
| ATTR024 | ENT004 | Country | country | character varying(40) | Yes | No | No | Country associated with the geography record. |
| ATTR025 | ENT005 | Partner Key | partner_key | integer | No | Yes | No | Surrogate key that uniquely identifies a partner record in the partner dimension. |
| ATTR026 | ENT005 | Partner ID | partner_id | character varying(20) | No | No | No | Business identifier assigned to the partner organization. |
| ATTR027 | ENT005 | Partner Name | partner_name | character varying(60) | Yes | No | No | Name of the partner organization involved in the transaction. |
| ATTR028 | ENT005 | Partner Type | partner_type | character varying(30) | Yes | No | No | Classifies the partner by operating model, such as distributor, reseller, systems integrator, or direct. |
| ATTR029 | ENT005 | Partner Tier | partner_tier | character varying(30) | Yes | No | No | Indicates the certification, authorization, or strategic tier assigned to the partner. |
| ATTR030 | ENT005 | Route to Market | route_to_market | character varying(20) | Yes | No | No | Describes the sales delivery path through which the product or service reached the customer. |
| ATTR031 | ENT006 | Product Key | product_key | integer | No | Yes | No | Surrogate key that uniquely identifies a product record in the product dimension. |
| ATTR032 | ENT006 | Product ID | product_id | character varying(30) | No | No | No | Business identifier or SKU assigned to the product or offer. |
| ATTR033 | ENT006 | Product Name | product_name | character varying(80) | Yes | No | No | Commercial name of the product or subscription offer sold to the customer. |
| ATTR034 | ENT006 | Product Family | product_family | character varying(30) | Yes | No | No | Higher-level product grouping used for portfolio and performance analysis. |
| ATTR035 | ENT006 | Technology Domain | technology_domain | character varying(40) | Yes | No | No | Technology area or solution domain to which the product belongs. |
| ATTR036 | ENT006 | Offer Type | offer_type | character varying(30) | Yes | No | No | Indicates whether the item is sold as hardware, software subscription, or SaaS subscription. |
| ATTR037 | ENT006 | Business Entity | business_entity | character varying(30) | Yes | No | No | Internal business unit or portfolio responsible for the product. |
| ATTR038 | ENT007 | Sales Representative Key | sales_rep_key | integer | No | Yes | No | Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. |
| ATTR039 | ENT007 | Sales Representative ID | rep_id | character varying(20) | No | No | No | Business identifier assigned to the sales representative. |
| ATTR040 | ENT007 | Sales Representative Name | rep_name | character varying(60) | Yes | No | No | Full name of the sales representative associated with the booking. |
| ATTR041 | ENT007 | Sales Role | sales_role | character varying(40) | Yes | No | No | Job role or account responsibility of the sales representative. |
| ATTR042 | ENT007 | Sales Team | sales_team | character varying(40) | Yes | No | No | Team or organizational unit to which the sales representative belongs. |
| ATTR043 | ENT007 | Covered Segment | segment_covered | character varying(30) | Yes | No | No | Customer segment for which the sales representative is responsible. |
| ATTR044 | ENT008 | Booking ID | booking_id | integer | No | Yes | No | Unique identifier for an individual booking transaction record. |
| ATTR045 | ENT008 | Order Number | order_number | character varying(20) | Yes | No | No | Business order number associated with the booking transaction. |
| ATTR046 | ENT008 | Order Line Number | order_line_number | integer | Yes | No | No | Line item number within the order associated with the booking. |
| ATTR047 | ENT008 | Booking Date Key | date_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the reporting date dimension. |
| ATTR048 | ENT008 | Customer Key | customer_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the customer dimension. |
| ATTR049 | ENT008 | Product Key | product_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the product dimension. |
| ATTR050 | ENT008 | Partner Key | partner_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the partner dimension. |
| ATTR051 | ENT008 | Geography Key | geography_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the geography dimension. |
| ATTR052 | ENT008 | Sales Representative Key | sales_rep_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the sales representative dimension. |
| ATTR053 | ENT008 | Contract Key | contract_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the contract dimension. |
| ATTR054 | ENT008 | Booking Type | booking_type | character varying(15) | Yes | No | No | Indicates whether the booking is a new sale or a renewal. |
| ATTR055 | ENT008 | Renewal Indicator | is_renewal | integer | Yes | No | No | Indicates whether the booking transaction is classified as a renewal. |
| ATTR056 | ENT008 | Quantity Sold | quantity | integer | Yes | No | No | Number of units, licenses, or subscriptions included in the booking transaction. |
| ATTR057 | ENT008 | Unit List Price USD | unit_list_price_usd | numeric | Yes | No | No | Standard list price per unit in U.S. dollars before discounts are applied. |
| ATTR058 | ENT008 | Discount Percentage | discount_pct | numeric | Yes | No | No | Percentage discount applied to the list price for the booking transaction. |
| ATTR059 | ENT008 | Booking Amount USD | booking_amount_usd | numeric | Yes | No | No | Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments. |
| ATTR060 | ENT008 | Annual Contract Value USD | acv_usd | numeric | Yes | No | No | Annualized value of the contract associated with the booking in U.S. dollars. |
| ATTR061 | ENT008 | Total Contract Value USD | tcv_usd | numeric | Yes | No | No | Total value of the full contract associated with the booking in U.S. dollars. |

## Measures

| Measure ID | Entity ID | Measure Name | Technical Column | Business Definition | Aggregation Type |
| --- | --- | --- | --- | --- | --- |
| MEA001 | ENT008 | Quantity Sold | quantity | Number of units, licenses, or subscriptions included in the booking transaction. | SUM |
| MEA002 | ENT008 | Unit List Price USD | unit_list_price_usd | Standard list price per unit in U.S. dollars before discounts are applied. | SUM |
| MEA003 | ENT008 | Discount Percentage | discount_pct | Percentage discount applied to the list price for the booking transaction. | AVG |
| MEA004 | ENT008 | Booking Amount USD | booking_amount_usd | Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments. | SUM |
| MEA005 | ENT008 | Annual Contract Value USD | acv_usd | Annualized value of the contract associated with the booking in U.S. dollars. | SUM |
| MEA006 | ENT008 | Total Contract Value USD | tcv_usd | Total value of the full contract associated with the booking in U.S. dollars. | SUM |

## Relationships

| Relationship ID | Parent Entity | Child Entity | Parent Attribute | Child Attribute | Relationship Type | Cardinality | Confidence Score |
| --- | --- | --- | --- | --- | --- | --- | --- |
| REL001 | Contract | Booking Transaction | Contract Key | Contract Key | Foreign Key | One-to-Many | 1.00 |
| REL002 | Customer | Booking Transaction | Customer Key | Customer Key | Foreign Key | One-to-Many | 1.00 |
| REL003 | Date | Booking Transaction | Date Key | Booking Date Key | Foreign Key | One-to-Many | 1.00 |
| REL004 | Geography | Booking Transaction | Geography Key | Geography Key | Foreign Key | One-to-Many | 1.00 |
| REL005 | Partner | Booking Transaction | Partner Key | Partner Key | Foreign Key | One-to-Many | 1.00 |
| REL006 | Product | Booking Transaction | Product Key | Product Key | Foreign Key | One-to-Many | 1.00 |
| REL007 | Sales Representative | Booking Transaction | Sales Representative Key | Sales Representative Key | Foreign Key | One-to-Many | 1.00 |

## Glossary Mapping

| Business Term | Business Definition | Technical Mapping | Entity | Attribute | Confidence Score |
| --- | --- | --- | --- | --- | --- |
| Contract | Stores the business attributes of commercial agreements associated with bookings, including contract type, term, renewal behavior, and support coverage level. | QuoteToBooking.dim_contract | Contract |  | 1.00 |
| Contract Key | Surrogate key that uniquely identifies a contract record in the contract dimension. | QuoteToBooking.dim_contract.contract_key | Contract | Contract Key | 1.00 |
| Contract Type | Describes the type of commercial agreement attached to the booking, such as SaaS subscription, Enterprise Agreement, or support contract. | QuoteToBooking.dim_contract.contract_type | Contract | Contract Type | 1.00 |
| Contract Term Months | Indicates the duration of the contract in months. | QuoteToBooking.dim_contract.term_months | Contract | Contract Term Months | 1.00 |
| Auto Renew Flag | Indicates whether the contract is set to renew automatically at the end of its term. | QuoteToBooking.dim_contract.auto_renew_flag | Contract | Auto Renew Flag | 1.00 |
| Coverage Level | Describes the level of service or support coverage provided under the contract. | QuoteToBooking.dim_contract.coverage_level | Contract | Coverage Level | 1.00 |
| Customer | Stores descriptive information about customers that place orders and generate bookings, including segment, industry, account tier, and headquarters location. | QuoteToBooking.dim_customer | Customer |  | 1.00 |
| Customer Key | Surrogate key that uniquely identifies a customer record in the customer dimension. | QuoteToBooking.dim_customer.customer_key | Customer | Customer Key | 1.00 |
| Customer ID | Business identifier assigned to the customer account. | QuoteToBooking.dim_customer.customer_id | Customer | Customer ID | 1.00 |
| Customer Name | Official name of the customer organization that purchased products or services. | QuoteToBooking.dim_customer.customer_name | Customer | Customer Name | 1.00 |
| Customer Segment | Classifies the customer into a business segment such as Enterprise, Service Provider, or Public Sector. | QuoteToBooking.dim_customer.segment | Customer | Customer Segment | 1.00 |
| Industry | Identifies the industry in which the customer operates. | QuoteToBooking.dim_customer.industry | Customer | Industry | 1.00 |
| Account Tier | Indicates the strategic importance or service tier of the customer account. | QuoteToBooking.dim_customer.account_tier | Customer | Account Tier | 1.00 |
| Headquarters Country | Country where the customer organization's headquarters is located. | QuoteToBooking.dim_customer.hq_country | Customer | Headquarters Country | 1.00 |
| Headquarters Region | Global region where the customer organization's headquarters is located. | QuoteToBooking.dim_customer.hq_region | Customer | Headquarters Region | 1.00 |
| Date | Stores calendar and fiscal date attributes used to analyze bookings over time. | QuoteToBooking.dim_date | Date |  | 1.00 |
| Date Key | Encoded key that uniquely identifies a reporting date in the date dimension. | QuoteToBooking.dim_date.date_key | Date | Date Key | 0.95 |
| Full Date | Actual calendar date represented by the date record. | QuoteToBooking.dim_date.full_date | Date | Full Date | 1.00 |
| Month Name | Name of the calendar month for the date. | QuoteToBooking.dim_date.month_name | Date | Month Name | 1.00 |
| Calendar Year | Four-digit calendar year associated with the date. | QuoteToBooking.dim_date.calendar_year | Date | Calendar Year | 1.00 |
| Fiscal Year | Fiscal year used by the business for financial and performance reporting. | QuoteToBooking.dim_date.fiscal_year | Date | Fiscal Year | 1.00 |
| Fiscal Quarter | Fiscal quarter used by the business for periodic reporting and analysis. | QuoteToBooking.dim_date.fiscal_quarter | Date | Fiscal Quarter | 1.00 |
| Fiscal Period Sequence | Sequential number representing the fiscal reporting period in ordered time analysis. | QuoteToBooking.dim_date.fiscal_period_seq | Date | Fiscal Period Sequence | 1.00 |
| Geography | Stores geographic attributes used to analyze bookings by sales region, theater, and country. | QuoteToBooking.dim_geography | Geography |  | 1.00 |
| Geography Key | Surrogate key that uniquely identifies a geography record in the geography dimension. | QuoteToBooking.dim_geography.geography_key | Geography | Geography Key | 1.00 |
| Sales Region | High-level geographic region used for reporting and performance analysis. | QuoteToBooking.dim_geography.region | Geography | Sales Region | 1.00 |
| Sales Theater | Subregional sales area or theater used to organize market coverage and reporting. | QuoteToBooking.dim_geography.theater | Geography | Sales Theater | 1.00 |
| Country | Country associated with the geography record. | QuoteToBooking.dim_geography.country | Geography | Country | 1.00 |
| Partner | Stores information about channel and direct partners involved in the sales process, including partner type, partner tier, and route to market. | QuoteToBooking.dim_partner | Partner |  | 1.00 |
| Partner Key | Surrogate key that uniquely identifies a partner record in the partner dimension. | QuoteToBooking.dim_partner.partner_key | Partner | Partner Key | 1.00 |
| Partner ID | Business identifier assigned to the partner organization. | QuoteToBooking.dim_partner.partner_id | Partner | Partner ID | 1.00 |
| Partner Name | Name of the partner organization involved in the transaction. | QuoteToBooking.dim_partner.partner_name | Partner | Partner Name | 1.00 |
| Partner Type | Classifies the partner by operating model, such as distributor, reseller, systems integrator, or direct. | QuoteToBooking.dim_partner.partner_type | Partner | Partner Type | 1.00 |
| Partner Tier | Indicates the certification, authorization, or strategic tier assigned to the partner. | QuoteToBooking.dim_partner.partner_tier | Partner | Partner Tier | 1.00 |
| Route to Market | Describes the sales delivery path through which the product or service reached the customer. | QuoteToBooking.dim_partner.route_to_market | Partner | Route to Market | 1.00 |
| Product | Stores descriptive information about products and offers sold to customers, including product family, technology domain, offer type, and business entity. | QuoteToBooking.dim_product | Product |  | 1.00 |
| Product Key | Surrogate key that uniquely identifies a product record in the product dimension. | QuoteToBooking.dim_product.product_key | Product | Product Key | 1.00 |
| Product ID | Business identifier or SKU assigned to the product or offer. | QuoteToBooking.dim_product.product_id | Product | Product ID | 1.00 |
| Product Name | Commercial name of the product or subscription offer sold to the customer. | QuoteToBooking.dim_product.product_name | Product | Product Name | 1.00 |
| Product Family | Higher-level product grouping used for portfolio and performance analysis. | QuoteToBooking.dim_product.product_family | Product | Product Family | 1.00 |
| Technology Domain | Technology area or solution domain to which the product belongs. | QuoteToBooking.dim_product.technology_domain | Product | Technology Domain | 1.00 |
| Offer Type | Indicates whether the item is sold as hardware, software subscription, or SaaS subscription. | QuoteToBooking.dim_product.offer_type | Product | Offer Type | 1.00 |
| Business Entity | Internal business unit or portfolio responsible for the product. | QuoteToBooking.dim_product.business_entity | Product | Business Entity | 1.00 |
| Sales Representative | Stores information about sales personnel responsible for managing customer relationships and booking transactions. | QuoteToBooking.dim_sales_rep | Sales Representative |  | 1.00 |
| Sales Representative Key | Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. | QuoteToBooking.dim_sales_rep.sales_rep_key | Sales Representative | Sales Representative Key | 1.00 |
| Sales Representative ID | Business identifier assigned to the sales representative. | QuoteToBooking.dim_sales_rep.rep_id | Sales Representative | Sales Representative ID | 1.00 |
| Sales Representative Name | Full name of the sales representative associated with the booking. | QuoteToBooking.dim_sales_rep.rep_name | Sales Representative | Sales Representative Name | 1.00 |
| Sales Role | Job role or account responsibility of the sales representative. | QuoteToBooking.dim_sales_rep.sales_role | Sales Representative | Sales Role | 1.00 |
| Sales Team | Team or organizational unit to which the sales representative belongs. | QuoteToBooking.dim_sales_rep.sales_team | Sales Representative | Sales Team | 1.00 |
| Covered Segment | Customer segment for which the sales representative is responsible. | QuoteToBooking.dim_sales_rep.segment_covered | Sales Representative | Covered Segment | 1.00 |
| Booking Transaction | Stores individual completed sales booking transactions with related financial measures and links to customer, product, partner, geography, sales representative, contract, and date dimensions. | QuoteToBooking.fact_bookings | Booking Transaction |  | 1.00 |
| Booking ID | Unique identifier for an individual booking transaction record. | QuoteToBooking.fact_bookings.booking_id | Booking Transaction | Booking ID | 1.00 |
| Order Number | Business order number associated with the booking transaction. | QuoteToBooking.fact_bookings.order_number | Booking Transaction | Order Number | 1.00 |
| Order Line Number | Line item number within the order associated with the booking. | QuoteToBooking.fact_bookings.order_line_number | Booking Transaction | Order Line Number | 1.00 |
| Booking Date Key | Foreign key linking the booking transaction to the reporting date dimension. | QuoteToBooking.fact_bookings.date_key | Booking Transaction | Booking Date Key | 1.00 |
| Booking Type | Indicates whether the booking is a new sale or a renewal. | QuoteToBooking.fact_bookings.booking_type | Booking Transaction | Booking Type | 1.00 |
| Renewal Indicator | Indicates whether the booking transaction is classified as a renewal. | QuoteToBooking.fact_bookings.is_renewal | Booking Transaction | Renewal Indicator | 0.95 |
| Quantity Sold | Number of units, licenses, or subscriptions included in the booking transaction. | QuoteToBooking.fact_bookings.quantity | Booking Transaction | Quantity Sold | 1.00 |
| Unit List Price USD | Standard list price per unit in U.S. dollars before discounts are applied. | QuoteToBooking.fact_bookings.unit_list_price_usd | Booking Transaction | Unit List Price USD | 1.00 |
| Discount Percentage | Percentage discount applied to the list price for the booking transaction. | QuoteToBooking.fact_bookings.discount_pct | Booking Transaction | Discount Percentage | 1.00 |
| Booking Amount USD | Total booked revenue amount for the transaction in U.S. dollars after pricing adjustments. | QuoteToBooking.fact_bookings.booking_amount_usd | Booking Transaction | Booking Amount USD | 1.00 |
| Annual Contract Value USD | Annualized value of the contract associated with the booking in U.S. dollars. | QuoteToBooking.fact_bookings.acv_usd | Booking Transaction | Annual Contract Value USD | 1.00 |
| Total Contract Value USD | Total value of the full contract associated with the booking in U.S. dollars. | QuoteToBooking.fact_bookings.tcv_usd | Booking Transaction | Total Contract Value USD | 1.00 |