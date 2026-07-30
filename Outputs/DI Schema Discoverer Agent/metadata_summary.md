# Metadata Summary

| Metric | Value |
| --- | --- |
| Database Type | PostgreSQL |
| Number of Schemas | 1 |
| Number of Tables | 8 |
| Number of Columns | 61 |
| Number of Primary Keys | 8 |
| Number of Foreign Keys | 7 |
| Number of Views | 0 |
| Number of Procedures/Functions | 0 |
| Number of Triggers | 0 |
| Number of Sequences | 0 |

## Relationships

| Parent Table | Child Table | Referenced Columns | Relationship Type |
| --- | --- | --- | --- |
| quotetobooking.dim_contract | quotetobooking.fact_bookings | contract_key -> contract_key | One-to-Many |
| quotetobooking.dim_customer | quotetobooking.fact_bookings | customer_key -> customer_key | One-to-Many |
| quotetobooking.dim_date | quotetobooking.fact_bookings | date_key -> date_key | One-to-Many |
| quotetobooking.dim_geography | quotetobooking.fact_bookings | geography_key -> geography_key | One-to-Many |
| quotetobooking.dim_partner | quotetobooking.fact_bookings | partner_key -> partner_key | One-to-Many |
| quotetobooking.dim_product | quotetobooking.fact_bookings | product_key -> product_key | One-to-Many |
| quotetobooking.dim_sales_rep | quotetobooking.fact_bookings | sales_rep_key -> sales_rep_key | One-to-Many |

## DDL Definitions

```sql
CREATE TABLE quotetobooking.dim_contract (
  contract_key INTEGER NOT NULL,
  contract_type VARCHAR(40),
  term_months INTEGER,
  auto_renew_flag CHARACTER(1),
  coverage_level VARCHAR(20)
);

CREATE TABLE quotetobooking.dim_customer (
  customer_key INTEGER NOT NULL,
  customer_id VARCHAR(20) NOT NULL,
  customer_name VARCHAR(80),
  segment VARCHAR(30),
  industry VARCHAR(40),
  account_tier VARCHAR(20),
  hq_country VARCHAR(40),
  hq_region VARCHAR(20)
);

CREATE TABLE quotetobooking.dim_date (
  date_key INTEGER NOT NULL,
  full_date DATE NOT NULL,
  month_name VARCHAR(12),
  calendar_year INTEGER,
  fiscal_year VARCHAR(6),
  fiscal_quarter VARCHAR(10),
  fiscal_period_seq INTEGER
);

CREATE TABLE quotetobooking.dim_geography (
  geography_key INTEGER NOT NULL,
  region VARCHAR(20),
  theater VARCHAR(30),
  country VARCHAR(40)
);

CREATE TABLE quotetobooking.dim_partner (
  partner_key INTEGER NOT NULL,
  partner_id VARCHAR(20) NOT NULL,
  partner_name VARCHAR(60),
  partner_type VARCHAR(30),
  partner_tier VARCHAR(30),
  route_to_market VARCHAR(20)
);

CREATE TABLE quotetobooking.dim_product (
  product_key INTEGER NOT NULL,
  product_id VARCHAR(30) NOT NULL,
  product_name VARCHAR(80),
  product_family VARCHAR(30),
  technology_domain VARCHAR(40),
  offer_type VARCHAR(30),
  business_entity VARCHAR(30)
);

CREATE TABLE quotetobooking.dim_sales_rep (
  sales_rep_key INTEGER NOT NULL,
  rep_id VARCHAR(20) NOT NULL,
  rep_name VARCHAR(60),
  sales_role VARCHAR(40),
  sales_team VARCHAR(40),
  segment_covered VARCHAR(30)
);

CREATE TABLE quotetobooking.fact_bookings (
  booking_id INTEGER NOT NULL,
  order_number VARCHAR(20),
  order_line_number INTEGER,
  date_key INTEGER,
  customer_key INTEGER,
  product_key INTEGER,
  partner_key INTEGER,
  geography_key INTEGER,
  sales_rep_key INTEGER,
  contract_key INTEGER,
  booking_type VARCHAR(15),
  is_renewal INTEGER,
  quantity INTEGER,
  unit_list_price_usd NUMERIC(12,2),
  discount_pct NUMERIC(5,2),
  booking_amount_usd NUMERIC(14,2),
  acv_usd NUMERIC(14,2),
  tcv_usd NUMERIC(14,2)
);

ALTER TABLE quotetobooking.dim_contract ADD CONSTRAINT dim_contract_pkey PRIMARY KEY (contract_key);
ALTER TABLE quotetobooking.dim_customer ADD CONSTRAINT dim_customer_pkey PRIMARY KEY (customer_key);
ALTER TABLE quotetobooking.dim_date ADD CONSTRAINT dim_date_pkey PRIMARY KEY (date_key);
ALTER TABLE quotetobooking.dim_geography ADD CONSTRAINT dim_geography_pkey PRIMARY KEY (geography_key);
ALTER TABLE quotetobooking.dim_partner ADD CONSTRAINT dim_partner_pkey PRIMARY KEY (partner_key);
ALTER TABLE quotetobooking.dim_product ADD CONSTRAINT dim_product_pkey PRIMARY KEY (product_key);
ALTER TABLE quotetobooking.dim_sales_rep ADD CONSTRAINT dim_sales_rep_pkey PRIMARY KEY (sales_rep_key);
ALTER TABLE quotetobooking.fact_bookings ADD CONSTRAINT fact_bookings_pkey PRIMARY KEY (booking_id);
ALTER TABLE quotetobooking.fact_bookings ADD CONSTRAINT fk_booking_contract FOREIGN KEY (contract_key) REFERENCES dim_contract(contract_key);
ALTER TABLE quotetobooking.fact_bookings ADD CONSTRAINT fk_booking_customer FOREIGN KEY (customer_key) REFERENCES dim_customer(customer_key);
ALTER TABLE quotetobooking.fact_bookings ADD CONSTRAINT fk_booking_date FOREIGN KEY (date_key) REFERENCES dim_date(date_key);
ALTER TABLE quotetobooking.fact_bookings ADD CONSTRAINT fk_booking_geography FOREIGN KEY (geography_key) REFERENCES dim_geography(geography_key);
ALTER TABLE quotetobooking.fact_bookings ADD CONSTRAINT fk_booking_partner FOREIGN KEY (partner_key) REFERENCES dim_partner(partner_key);
ALTER TABLE quotetobooking.fact_bookings ADD CONSTRAINT fk_booking_product FOREIGN KEY (product_key) REFERENCES dim_product(product_key);
ALTER TABLE quotetobooking.fact_bookings ADD CONSTRAINT fk_booking_sales_rep FOREIGN KEY (sales_rep_key) REFERENCES dim_sales_rep(sales_rep_key);

CREATE UNIQUE INDEX dim_contract_pkey ON quotetobooking.dim_contract USING btree (contract_key);
CREATE UNIQUE INDEX dim_customer_pkey ON quotetobooking.dim_customer USING btree (customer_key);
CREATE UNIQUE INDEX dim_date_pkey ON quotetobooking.dim_date USING btree (date_key);
CREATE UNIQUE INDEX dim_geography_pkey ON quotetobooking.dim_geography USING btree (geography_key);
CREATE UNIQUE INDEX dim_partner_pkey ON quotetobooking.dim_partner USING btree (partner_key);
CREATE UNIQUE INDEX dim_product_pkey ON quotetobooking.dim_product USING btree (product_key);
CREATE UNIQUE INDEX dim_sales_rep_pkey ON quotetobooking.dim_sales_rep USING btree (sales_rep_key);
CREATE UNIQUE INDEX fact_bookings_pkey ON quotetobooking.fact_bookings USING btree (booking_id);
```