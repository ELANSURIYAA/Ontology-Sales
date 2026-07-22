## Domains

| Domain ID | Domain Name | Description |
| --- | --- | --- |
| DOM001 | Sales Bookings and Revenue Analytics | Supports analysis of completed sales bookings for enterprise products and subscription services across customers, products, partners, geographies, sales representatives, contracts, and fiscal periods. |

---

## Entities

| Entity ID | Domain ID | Business Name | Technical Table Name | Description | Business Keys |
| --- | --- | --- | --- | --- | --- |
| ENT001 | DOM001 | Contract | QuoteToBooking.dim_contract | Stores the contractual attributes associated with a booking, including agreement type, duration, renewal behavior, and support or service coverage level. | contract_key |
| ENT002 | DOM001 | Customer | QuoteToBooking.dim_customer | Stores customer master data used to analyze bookings by customer identity, market segment, industry, account tier, and headquarters location. | customer_key; customer_id |
| ENT003 | DOM001 | Date | QuoteToBooking.dim_date | Stores calendar and fiscal date attributes used to analyze bookings over time and support period-based reporting. | date_key |
| ENT004 | DOM001 | Geography | QuoteToBooking.dim_geography | Stores geographic attributes used to analyze bookings across sales regions, theaters, and countries. | geography_key |
| ENT005 | DOM001 | Partner | QuoteToBooking.dim_partner | Stores partner master data used to analyze indirect and direct sales activity by partner identity, partner type, tier, and route to market. | partner_key; partner_id |
| ENT006 | DOM001 | Product | QuoteToBooking.dim_product | Stores product master data used to analyze bookings by product identity, family, technology domain, offer type, and business entity. | product_key; product_id |
| ENT007 | DOM001 | Sales Representative | QuoteToBooking.dim_sales_rep | Stores sales representative attributes used to analyze bookings by individual seller, role, team, and covered segment. | sales_rep_key; rep_id |
| ENT008 | DOM001 | Booking Transaction | QuoteToBooking.fact_bookings | Stores individual completed sales booking transactions and their associated financial measures, linked to customer, product, partner, geography, sales representative, contract, and date dimensions. | booking_id; order_number; order_line_number |

---

## Attributes

| Attribute ID | Entity ID | Business Attribute | Technical Column | Data Type | Nullable | Primary Key | Foreign Key | Description |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ATT001 | ENT001 | Contract Key | contract_key | integer | No | Yes | No | Surrogate key that uniquely identifies a contract record in the contract dimension. |
| ATT002 | ENT001 | Contract Type | contract_type | character varying | Yes | No | No | Indicates the type of commercial agreement or service contract associated with the booking, such as SaaS Subscription or Enterprise Agreement. |
| ATT003 | ENT001 | Contract Term Months | term_months | integer | Yes | No | No | Specifies the duration of the contract in months. |
| ATT004 | ENT001 | Auto Renew Indicator | auto_renew_flag | character | Yes | No | No | Indicates whether the contract is configured to renew automatically. |
| ATT005 | ENT001 | Coverage Level | coverage_level | character varying | Yes | No | No | Describes the support, service, or entitlement coverage level provided under the contract. |
| ATT006 | ENT002 | Customer Key | customer_key | integer | No | Yes | No | Surrogate key that uniquely identifies a customer record in the customer dimension. |
| ATT007 | ENT002 | Customer ID | customer_id | character varying | No | No | No | Business identifier assigned to the customer account. |
| ATT008 | ENT002 | Customer Name | customer_name | character varying | Yes | No | No | Name of the customer organization associated with the booking. |
| ATT009 | ENT002 | Customer Segment | segment | character varying | Yes | No | No | Classifies the customer into a business segment such as Enterprise, Service Provider, or Public Sector. |
| ATT010 | ENT002 | Industry | industry | character varying | Yes | No | No | Indicates the customer’s industry classification for business analysis. |
| ATT011 | ENT002 | Account Tier | account_tier | character varying | Yes | No | No | Identifies the strategic importance or service tier of the customer account. |
| ATT012 | ENT002 | Headquarters Country | hq_country | character varying | Yes | No | No | Country where the customer’s headquarters is located. |
| ATT013 | ENT002 | Headquarters Region | hq_region | character varying | Yes | No | No | Region where the customer’s headquarters is located, such as Americas, EMEA, or APJC. |
| ATT014 | ENT003 | Date Key | date_key | integer | No | Yes | No | Encoded key that uniquely identifies a date record in the date dimension. |
| ATT015 | ENT003 | Full Date | full_date | date | No | No | No | Calendar date represented by the date dimension record. |
| ATT016 | ENT003 | Month Name | month_name | character varying | Yes | No | No | Name of the calendar month for the date. |
| ATT017 | ENT003 | Calendar Year | calendar_year | integer | Yes | No | No | Four-digit calendar year associated with the date. |
| ATT018 | ENT003 | Fiscal Year | fiscal_year | character varying | Yes | No | No | Fiscal year used for business reporting and performance analysis. |
| ATT019 | ENT003 | Fiscal Quarter | fiscal_quarter | character varying | Yes | No | No | Fiscal quarter used for reporting and period-based business analysis. |
| ATT020 | ENT003 | Fiscal Period Sequence | fiscal_period_seq | integer | Yes | No | No | Sequential number representing the order of the fiscal period in the reporting calendar. |
| ATT021 | ENT004 | Geography Key | geography_key | integer | No | Yes | No | Surrogate key that uniquely identifies a geography record in the geography dimension. |
| ATT022 | ENT004 | Sales Region | region | character varying | Yes | No | No | High-level geographic region used for business reporting and sales analysis. |
| ATT023 | ENT004 | Sales Theater | theater | character varying | Yes | No | No | Intermediate geographic sales area within a region used for operational reporting. |
| ATT024 | ENT004 | Country | country | character varying | Yes | No | No | Country associated with the geography record for booking analysis. |
| ATT025 | ENT005 | Partner Key | partner_key | integer | No | Yes | No | Surrogate key that uniquely identifies a partner record in the partner dimension. |
| ATT026 | ENT005 | Partner ID | partner_id | character varying | No | No | No | Business identifier assigned to the partner organization. |
| ATT027 | ENT005 | Partner Name | partner_name | character varying | Yes | No | No | Name of the partner organization involved in the sale or fulfillment process. |
| ATT028 | ENT005 | Partner Type | partner_type | character varying | Yes | No | No | Classifies the partner by business role, such as distributor, reseller, systems integrator, or direct. |
| ATT029 | ENT005 | Partner Tier | partner_tier | character varying | Yes | No | No | Indicates the partner’s program tier or accreditation level. |
| ATT030 | ENT005 | Route to Market | route_to_market | character varying | Yes | No | No | Describes the sales channel path through which the offering reaches the customer. |
| ATT031 | ENT006 | Product Key | product_key | integer | No | Yes | No | Surrogate key that uniquely identifies a product record in the product dimension. |
| ATT032 | ENT006 | Product ID | product_id | character varying | No | No | No | Business identifier or SKU assigned to the product or offering. |
| ATT033 | ENT006 | Product Name | product_name | character varying | Yes | No | No | Name of the product, solution, or subscription offering. |
| ATT034 | ENT006 | Product Family | product_family | character varying | Yes | No | No | Groups related products into a common family for portfolio analysis. |
| ATT035 | ENT006 | Technology Domain | technology_domain | character varying | Yes | No | No | Identifies the technology area associated with the product, such as networking, security, or collaboration. |
| ATT036 | ENT006 | Offer Type | offer_type | character varying | Yes | No | No | Indicates whether the offering is hardware, software subscription, or SaaS subscription. |
| ATT037 | ENT006 | Business Entity | business_entity | character varying | Yes | No | No | Identifies the internal business unit or portfolio associated with the product. |
| ATT038 | ENT007 | Sales Representative Key | sales_rep_key | integer | No | Yes | No | Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. |
| ATT039 | ENT007 | Sales Representative ID | rep_id | character varying | No | No | No | Business identifier assigned to the sales representative. |
| ATT040 | ENT007 | Sales Representative Name | rep_name | character varying | Yes | No | No | Full name of the sales representative responsible for the customer relationship or sale. |
| ATT041 | ENT007 | Sales Role | sales_role | character varying | Yes | No | No | Job role or selling responsibility of the sales representative. |
| ATT042 | ENT007 | Sales Team | sales_team | character varying | Yes | No | No | Team or organizational unit to which the sales representative belongs. |
| ATT043 | ENT007 | Covered Segment | segment_covered | character varying | Yes | No | No | Customer segment for which the sales representative is responsible. |
| ATT044 | ENT008 | Booking ID | booking_id | integer | No | Yes | No | Unique identifier for the booking transaction record. |
| ATT045 | ENT008 | Order Number | order_number | character varying | Yes | No | No | Business order number associated with the booking transaction. |
| ATT046 | ENT008 | Order Line Number | order_line_number | integer | Yes | No | No | Line number within the order associated with the booking transaction. |
| ATT047 | ENT008 | Booking Date Key | date_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the date dimension. |
| ATT048 | ENT008 | Customer Key | customer_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the customer dimension. |
| ATT049 | ENT008 | Product Key | product_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the product dimension. |
| ATT050 | ENT008 | Partner Key | partner_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the partner dimension. |
| ATT051 | ENT008 | Geography Key | geography_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the geography dimension. |
| ATT052 | ENT008 | Sales Representative Key | sales_rep_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the sales representative dimension. |
| ATT053 | ENT008 | Contract Key | contract_key | integer | Yes | No | Yes | Foreign key linking the booking transaction to the contract dimension. |
| ATT054 | ENT008 | Booking Type | booking_type | character varying | Yes | No | No | Indicates whether the booking is a new sale or a renewal. |
| ATT055 | ENT008 | Renewal Indicator | is_renewal | integer | Yes | No | No | Indicates whether the booking transaction represents a renewal event. |
| ATT056 | ENT008 | Quantity Sold | quantity | integer | Yes | No | No | Number of units, licenses, or service quantities included in the booking. |
| ATT057 | ENT008 | Unit List Price USD | unit_list_price_usd | numeric | Yes | No | No | Standard list price per unit in U.S. dollars before discounts. |
| ATT058 | ENT008 | Discount Percentage | discount_pct | numeric | Yes | No | No | Discount applied to the list price for the booking transaction. |
| ATT059 | ENT008 | Booking Amount USD | booking_amount_usd | numeric | Yes | No | No | Total booked sales value recognized for the transaction in U.S. dollars. |
| ATT060 | ENT008 | Annual Contract Value USD | acv_usd | numeric | Yes | No | No | Annualized value of the contract associated with the booking in U.S. dollars. |
| ATT061 | ENT008 | Total Contract Value USD | tcv_usd | numeric | Yes | No | No | Total contract value associated with the booking in U.S. dollars over the contract term. |

---

## Measures

| Measure ID | Entity ID | Measure Name | Technical Column | Business Definition | Aggregation Type |
| --- | --- | --- | --- | --- | --- |
| MEA001 | ENT008 | Quantity Sold | quantity | Number of units, licenses, or service quantities included in the booking. | Sum |
| MEA002 | ENT008 | Unit List Price USD | unit_list_price_usd | Standard list price per unit in U.S. dollars before discounts. | Average |
| MEA003 | ENT008 | Discount Percentage | discount_pct | Discount applied to the list price for the booking transaction. | Average |
| MEA004 | ENT008 | Booking Amount USD | booking_amount_usd | Total booked sales value recognized for the transaction in U.S. dollars. | Sum |
| MEA005 | ENT008 | Annual Contract Value USD | acv_usd | Annualized value of the contract associated with the booking in U.S. dollars. | Sum |
| MEA006 | ENT008 | Total Contract Value USD | tcv_usd | Total contract value associated with the booking in U.S. dollars over the contract term. | Sum |

---

## Relationships

| Relationship ID | Parent Entity | Child Entity | Parent Attribute | Child Attribute | Relationship Type | Cardinality | Confidence Score |
| --- | --- | --- | --- | --- | --- | --- | --- |
| REL001 | Contract | Booking Transaction | Contract Key | Contract Key | Referential | One-to-Many | 1.00 |
| REL002 | Customer | Booking Transaction | Customer Key | Customer Key | Referential | One-to-Many | 1.00 |
| REL003 | Date | Booking Transaction | Date Key | Booking Date Key | Referential | One-to-Many | 1.00 |
| REL004 | Geography | Booking Transaction | Geography Key | Geography Key | Referential | One-to-Many | 1.00 |
| REL005 | Partner | Booking Transaction | Partner Key | Partner Key | Referential | One-to-Many | 1.00 |
| REL006 | Product | Booking Transaction | Product Key | Product Key | Referential | One-to-Many | 1.00 |
| REL007 | Sales Representative | Booking Transaction | Sales Representative Key | Sales Representative Key | Referential | One-to-Many | 1.00 |

---

## Glossary Mapping

| Business Term | Business Definition | Technical Mapping | Entity | Attribute | Confidence Score |
| --- | --- | --- | --- | --- | --- |
| Contract | Stores the contractual attributes associated with a booking, including agreement type, duration, renewal behavior, and support or service coverage level. | QuoteToBooking.dim_contract | Contract |  | 1.00 |
| Contract Key | Surrogate key that uniquely identifies a contract record in the contract dimension. | QuoteToBooking.dim_contract.contract_key | Contract | Contract Key | 1.00 |
| Contract Type | Indicates the type of commercial agreement or service contract associated with the booking, such as SaaS Subscription or Enterprise Agreement. | QuoteToBooking.dim_contract.contract_type | Contract | Contract Type | 1.00 |
| Contract Term Months | Specifies the duration of the contract in months. | QuoteToBooking.dim_contract.term_months | Contract | Contract Term Months | 1.00 |
| Auto Renew Indicator | Indicates whether the contract is configured to renew automatically. | QuoteToBooking.dim_contract.auto_renew_flag | Contract | Auto Renew Indicator | 1.00 |
| Coverage Level | Describes the support, service, or entitlement coverage level provided under the contract. | QuoteToBooking.dim_contract.coverage_level | Contract | Coverage Level | 1.00 |
| Customer | Stores customer master data used to analyze bookings by customer identity, market segment, industry, account tier, and headquarters location. | QuoteToBooking.dim_customer | Customer |  | 1.00 |
| Customer Key | Surrogate key that uniquely identifies a customer record in the customer dimension. | QuoteToBooking.dim_customer.customer_key; QuoteToBooking.fact_bookings.customer_key | Customer; Booking Transaction | Customer Key | 1.00 |
| Customer ID | Business identifier assigned to the customer account. | QuoteToBooking.dim_customer.customer_id | Customer | Customer ID | 1.00 |
| Customer Name | Name of the customer organization associated with the booking. | QuoteToBooking.dim_customer.customer_name | Customer | Customer Name | 1.00 |
| Customer Segment | Classifies the customer into a business segment such as Enterprise, Service Provider, or Public Sector. | QuoteToBooking.dim_customer.segment | Customer | Customer Segment | 1.00 |
| Industry | Indicates the customer’s industry classification for business analysis. | QuoteToBooking.dim_customer.industry | Customer | Industry | 1.00 |
| Account Tier | Identifies the strategic importance or service tier of the customer account. | QuoteToBooking.dim_customer.account_tier | Customer | Account Tier | 1.00 |
| Headquarters Country | Country where the customer’s headquarters is located. | QuoteToBooking.dim_customer.hq_country | Customer | Headquarters Country | 1.00 |
| Headquarters Region | Region where the customer’s headquarters is located, such as Americas, EMEA, or APJC. | QuoteToBooking.dim_customer.hq_region | Customer | Headquarters Region | 1.00 |
| Date | Stores calendar and fiscal date attributes used to analyze bookings over time and support period-based reporting. | QuoteToBooking.dim_date | Date |  | 1.00 |
| Date Key | Encoded key that uniquely identifies a date record in the date dimension. | QuoteToBooking.dim_date.date_key; QuoteToBooking.fact_bookings.date_key | Date; Booking Transaction | Date Key; Booking Date Key | 0.95 |
| Full Date | Calendar date represented by the date dimension record. | QuoteToBooking.dim_date.full_date | Date | Full Date | 1.00 |
| Month Name | Name of the calendar month for the date. | QuoteToBooking.dim_date.month_name | Date | Month Name | 1.00 |
| Calendar Year | Four-digit calendar year associated with the date. | QuoteToBooking.dim_date.calendar_year | Date | Calendar Year | 1.00 |
| Fiscal Year | Fiscal year used for business reporting and performance analysis. | QuoteToBooking.dim_date.fiscal_year | Date | Fiscal Year | 1.00 |
| Fiscal Quarter | Fiscal quarter used for reporting and period-based business analysis. | QuoteToBooking.dim_date.fiscal_quarter | Date | Fiscal Quarter | 1.00 |
| Fiscal Period Sequence | Sequential number representing the order of the fiscal period in the reporting calendar. | QuoteToBooking.dim_date.fiscal_period_seq | Date | Fiscal Period Sequence | 1.00 |
| Geography | Stores geographic attributes used to analyze bookings across sales regions, theaters, and countries. | QuoteToBooking.dim_geography | Geography |  | 1.00 |
| Geography Key | Surrogate key that uniquely identifies a geography record in the geography dimension. | QuoteToBooking.dim_geography.geography_key; QuoteToBooking.fact_bookings.geography_key | Geography; Booking Transaction | Geography Key | 1.00 |
| Sales Region | High-level geographic region used for business reporting and sales analysis. | QuoteToBooking.dim_geography.region | Geography | Sales Region | 1.00 |
| Sales Theater | Intermediate geographic sales area within a region used for operational reporting. | QuoteToBooking.dim_geography.theater | Geography | Sales Theater | 1.00 |
| Country | Country associated with the geography record for booking analysis. | QuoteToBooking.dim_geography.country | Geography | Country | 1.00 |
| Partner | Stores partner master data used to analyze indirect and direct sales activity by partner identity, partner type, tier, and route to market. | QuoteToBooking.dim_partner | Partner |  | 1.00 |
| Partner Key | Surrogate key that uniquely identifies a partner record in the partner dimension. | QuoteToBooking.dim_partner.partner_key; QuoteToBooking.fact_bookings.partner_key | Partner; Booking Transaction | Partner Key | 1.00 |
| Partner ID | Business identifier assigned to the partner organization. | QuoteToBooking.dim_partner.partner_id | Partner | Partner ID | 1.00 |
| Partner Name | Name of the partner organization involved in the sale or fulfillment process. | QuoteToBooking.dim_partner.partner_name | Partner | Partner Name | 1.00 |
| Partner Type | Classifies the partner by business role, such as distributor, reseller, systems integrator, or direct. | QuoteToBooking.dim_partner.partner_type | Partner | Partner Type | 1.00 |
| Partner Tier | Indicates the partner’s program tier or accreditation level. | QuoteToBooking.dim_partner.partner_tier | Partner | Partner Tier | 1.00 |
| Route to Market | Describes the sales channel path through which the offering reaches the customer. | QuoteToBooking.dim_partner.route_to_market | Partner | Route to Market | 1.00 |
| Product | Stores product master data used to analyze bookings by product identity, family, technology domain, offer type, and business entity. | QuoteToBooking.dim_product | Product |  | 1.00 |
| Product Key | Surrogate key that uniquely identifies a product record in the product dimension. | QuoteToBooking.dim_product.product_key; QuoteToBooking.fact_bookings.product_key | Product; Booking Transaction | Product Key | 1.00 |
| Product ID | Business identifier or SKU assigned to the product or offering. | QuoteToBooking.dim_product.product_id | Product | Product ID | 1.00 |
| Product Name | Name of the product, solution, or subscription offering. | QuoteToBooking.dim_product.product_name | Product | Product Name | 1.00 |
| Product Family | Groups related products into a common family for portfolio analysis. | QuoteToBooking.dim_product.product_family | Product | Product Family | 1.00 |
| Technology Domain | Identifies the technology area associated with the product, such as networking, security, or collaboration. | QuoteToBooking.dim_product.technology_domain | Product | Technology Domain | 1.00 |
| Offer Type | Indicates whether the offering is hardware, software subscription, or SaaS subscription. | QuoteToBooking.dim_product.offer_type | Product | Offer Type | 1.00 |
| Business Entity | Identifies the internal business unit or portfolio associated with the product. | QuoteToBooking.dim_product.business_entity | Product | Business Entity | 1.00 |
| Sales Representative | Stores sales representative attributes used to analyze bookings by individual seller, role, team, and covered segment. | QuoteToBooking.dim_sales_rep | Sales Representative |  | 1.00 |
| Sales Representative Key | Surrogate key that uniquely identifies a sales representative record in the sales representative dimension. | QuoteToBooking.dim_sales_rep.sales_rep_key; QuoteToBooking.fact_bookings.sales_rep_key | Sales Representative; Booking Transaction | Sales Representative Key | 1.00 |
| Sales Representative ID | Business identifier assigned to the sales representative. | QuoteToBooking.dim_sales_rep.rep_id | Sales Representative | Sales Representative ID | 1.00 |
| Sales Representative Name | Full name of the sales representative responsible for the customer relationship or sale. | QuoteToBooking.dim_sales_rep.rep_name | Sales Representative | Sales Representative Name | 1.00 |
| Sales Role | Job role or selling responsibility of the sales representative. | QuoteToBooking.dim_sales_rep.sales_role | Sales Representative | Sales Role | 1.00 |
| Sales Team | Team or organizational unit to which the sales representative belongs. | QuoteToBooking.dim_sales_rep.sales_team | Sales Representative | Sales Team | 1.00 |
| Covered Segment | Customer segment for which the sales representative is responsible. | QuoteToBooking.dim_sales_rep.segment_covered | Sales Representative | Covered Segment | 1.00 |
| Booking Transaction | Stores individual completed sales booking transactions and their associated financial measures, linked to customer, product, partner, geography, sales representative, contract, and date dimensions. | QuoteToBooking.fact_bookings | Booking Transaction |  | 1.00 |
| Booking ID | Unique identifier for the booking transaction record. | QuoteToBooking.fact_bookings.booking_id | Booking Transaction | Booking ID | 1.00 |
| Order Number | Business order number associated with the booking transaction. | QuoteToBooking.fact_bookings.order_number | Booking Transaction | Order Number | 1.00 |
| Order Line Number | Line number within the order associated with the booking transaction. | QuoteToBooking.fact_bookings.order_line_number | Booking Transaction | Order Line Number | 1.00 |
| Booking Date Key | Foreign key linking the booking transaction to the date dimension. | QuoteToBooking.fact_bookings.date_key | Booking Transaction | Booking Date Key | 1.00 |
| Booking Type | Indicates whether the booking is a new sale or a renewal. | QuoteToBooking.fact_bookings.booking_type | Booking Transaction | Booking Type | 1.00 |
| Renewal Indicator | Indicates whether the booking transaction represents a renewal event. | QuoteToBooking.fact_bookings.is_renewal | Booking Transaction | Renewal Indicator | 1.00 |
| Quantity Sold | Number of units, licenses, or service quantities included in the booking. | QuoteToBooking.fact_bookings.quantity | Booking Transaction | Quantity Sold | 1.00 |
| Unit List Price USD | Standard list price per unit in U.S. dollars before discounts. | QuoteToBooking.fact_bookings.unit_list_price_usd | Booking Transaction | Unit List Price USD | 1.00 |
| Discount Percentage | Discount applied to the list price for the booking transaction. | QuoteToBooking.fact_bookings.discount_pct | Booking Transaction | Discount Percentage | 1.00 |
| Booking Amount USD | Total booked sales value recognized for the transaction in U.S. dollars. | QuoteToBooking.fact_bookings.booking_amount_usd | Booking Transaction | Booking Amount USD | 1.00 |
| Annual Contract Value USD | Annualized value of the contract associated with the booking in U.S. dollars. | QuoteToBooking.fact_bookings.acv_usd | Booking Transaction | Annual Contract Value USD | 1.00 |
| Total Contract Value USD | Total contract value associated with the booking in U.S. dollars over the contract term. | QuoteToBooking.fact_bookings.tcv_usd | Booking Transaction | Total Contract Value USD | 1.00 |