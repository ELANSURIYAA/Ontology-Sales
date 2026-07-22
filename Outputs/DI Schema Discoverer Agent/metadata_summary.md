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
| QuoteToBooking.dim_contract | QuoteToBooking.fact_bookings | contract_key -> contract_key | One-to-Many |
| QuoteToBooking.dim_customer | QuoteToBooking.fact_bookings | customer_key -> customer_key | One-to-Many |
| QuoteToBooking.dim_date | QuoteToBooking.fact_bookings | date_key -> date_key | One-to-Many |
| QuoteToBooking.dim_geography | QuoteToBooking.fact_bookings | geography_key -> geography_key | One-to-Many |
| QuoteToBooking.dim_partner | QuoteToBooking.fact_bookings | partner_key -> partner_key | One-to-Many |
| QuoteToBooking.dim_product | QuoteToBooking.fact_bookings | product_key -> product_key | One-to-Many |
| QuoteToBooking.dim_sales_rep | QuoteToBooking.fact_bookings | sales_rep_key -> sales_rep_key | One-to-Many |

## DDL Definitions

```sql
CREATE TABLE "QuoteToBooking".dim_contract (
  contract_key integer NOT NULL,
  contract_type character varying,
  term_months integer,
  auto_renew_flag character,
  coverage_level character varying,
  CONSTRAINT dim_contract_pkey PRIMARY KEY (contract_key)
);

CREATE TABLE "QuoteToBooking".dim_customer (
  customer_key integer NOT NULL,
  customer_id character varying NOT NULL,
  customer_name character varying,
  segment character varying,
  industry character varying,
  account_tier character varying,
  hq_country character varying,
  hq_region character varying,
  CONSTRAINT dim_customer_pkey PRIMARY KEY (customer_key)
);

CREATE TABLE "QuoteToBooking".dim_date (
  date_key integer NOT NULL,
  full_date date NOT NULL,
  month_name character varying,
  calendar_year integer,
  fiscal_year character varying,
  fiscal_quarter character varying,
  fiscal_period_seq integer,
  CONSTRAINT dim_date_pkey PRIMARY KEY (date_key)
);

CREATE TABLE "QuoteToBooking".dim_geography (
  geography_key integer NOT NULL,
  region character varying,
  theater character varying,
  country character varying,
  CONSTRAINT dim_geography_pkey PRIMARY KEY (geography_key)
);

CREATE TABLE "QuoteToBooking".dim_partner (
  partner_key integer NOT NULL,
  partner_id character varying NOT NULL,
  partner_name character varying,
  partner_type character varying,
  partner_tier character varying,
  route_to_market character varying,
  CONSTRAINT dim_partner_pkey PRIMARY KEY (partner_key)
);

CREATE TABLE "QuoteToBooking".dim_product (
  product_key integer NOT NULL,
  product_id character varying NOT NULL,
  product_name character varying,
  product_family character varying,
  technology_domain character varying,
  offer_type character varying,
  business_entity character varying,
  CONSTRAINT dim_product_pkey PRIMARY KEY (product_key)
);

CREATE TABLE "QuoteToBooking".dim_sales_rep (
  sales_rep_key integer NOT NULL,
  rep_id character varying NOT NULL,
  rep_name character varying,
  sales_role character varying,
  sales_team character varying,
  segment_covered character varying,
  CONSTRAINT dim_sales_rep_pkey PRIMARY KEY (sales_rep_key)
);

CREATE TABLE "QuoteToBooking".fact_bookings (
  booking_id integer NOT NULL,
  order_number character varying,
  order_line_number integer,
  date_key integer,
  customer_key integer,
  product_key integer,
  partner_key integer,
  geography_key integer,
  sales_rep_key integer,
  contract_key integer,
  booking_type character varying,
  is_renewal integer,
  quantity integer,
  unit_list_price_usd numeric,
  discount_pct numeric,
  booking_amount_usd numeric,
  acv_usd numeric,
  tcv_usd numeric,
  CONSTRAINT fact_bookings_pkey PRIMARY KEY (booking_id),
  CONSTRAINT fk_booking_contract FOREIGN KEY (contract_key) REFERENCES "QuoteToBooking".dim_contract(contract_key),
  CONSTRAINT fk_booking_customer FOREIGN KEY (customer_key) REFERENCES "QuoteToBooking".dim_customer(customer_key),
  CONSTRAINT fk_booking_date FOREIGN KEY (date_key) REFERENCES "QuoteToBooking".dim_date(date_key),
  CONSTRAINT fk_booking_geography FOREIGN KEY (geography_key) REFERENCES "QuoteToBooking".dim_geography(geography_key),
  CONSTRAINT fk_booking_partner FOREIGN KEY (partner_key) REFERENCES "QuoteToBooking".dim_partner(partner_key),
  CONSTRAINT fk_booking_product FOREIGN KEY (product_key) REFERENCES "QuoteToBooking".dim_product(product_key),
  CONSTRAINT fk_booking_sales_rep FOREIGN KEY (sales_rep_key) REFERENCES "QuoteToBooking".dim_sales_rep(sales_rep_key)
);

ALTER TABLE "QuoteToBooking".dim_contract ADD CONSTRAINT dim_contract_pkey PRIMARY KEY (contract_key);
ALTER TABLE "QuoteToBooking".dim_customer ADD CONSTRAINT dim_customer_pkey PRIMARY KEY (customer_key);
ALTER TABLE "QuoteToBooking".dim_date ADD CONSTRAINT dim_date_pkey PRIMARY KEY (date_key);
ALTER TABLE "QuoteToBooking".dim_geography ADD CONSTRAINT dim_geography_pkey PRIMARY KEY (geography_key);
ALTER TABLE "QuoteToBooking".dim_partner ADD CONSTRAINT dim_partner_pkey PRIMARY KEY (partner_key);
ALTER TABLE "QuoteToBooking".dim_product ADD CONSTRAINT dim_product_pkey PRIMARY KEY (product_key);
ALTER TABLE "QuoteToBooking".dim_sales_rep ADD CONSTRAINT dim_sales_rep_pkey PRIMARY KEY (sales_rep_key);
ALTER TABLE "QuoteToBooking".fact_bookings ADD CONSTRAINT fact_bookings_pkey PRIMARY KEY (booking_id);
ALTER TABLE "QuoteToBooking".fact_bookings ADD CONSTRAINT fk_booking_contract FOREIGN KEY (contract_key) REFERENCES "QuoteToBooking".dim_contract(contract_key);
ALTER TABLE "QuoteToBooking".fact_bookings ADD CONSTRAINT fk_booking_customer FOREIGN KEY (customer_key) REFERENCES "QuoteToBooking".dim_customer(customer_key);
ALTER TABLE "QuoteToBooking".fact_bookings ADD CONSTRAINT fk_booking_date FOREIGN KEY (date_key) REFERENCES "QuoteToBooking".dim_date(date_key);
ALTER TABLE "QuoteToBooking".fact_bookings ADD CONSTRAINT fk_booking_geography FOREIGN KEY (geography_key) REFERENCES "QuoteToBooking".dim_geography(geography_key);
ALTER TABLE "QuoteToBooking".fact_bookings ADD CONSTRAINT fk_booking_partner FOREIGN KEY (partner_key) REFERENCES "QuoteToBooking".dim_partner(partner_key);
ALTER TABLE "QuoteToBooking".fact_bookings ADD CONSTRAINT fk_booking_product FOREIGN KEY (product_key) REFERENCES "QuoteToBooking".dim_product(product_key);
ALTER TABLE "QuoteToBooking".fact_bookings ADD CONSTRAINT fk_booking_sales_rep FOREIGN KEY (sales_rep_key) REFERENCES "QuoteToBooking".dim_sales_rep(sales_rep_key);

CREATE UNIQUE INDEX dim_contract_pkey ON "QuoteToBooking".dim_contract USING btree (contract_key);
CREATE UNIQUE INDEX dim_customer_pkey ON "QuoteToBooking".dim_customer USING btree (customer_key);
CREATE UNIQUE INDEX dim_date_pkey ON "QuoteToBooking".dim_date USING btree (date_key);
CREATE UNIQUE INDEX dim_geography_pkey ON "QuoteToBooking".dim_geography USING btree (geography_key);
CREATE UNIQUE INDEX dim_partner_pkey ON "QuoteToBooking".dim_partner USING btree (partner_key);
CREATE UNIQUE INDEX dim_product_pkey ON "QuoteToBooking".dim_product USING btree (product_key);
CREATE UNIQUE INDEX dim_sales_rep_pkey ON "QuoteToBooking".dim_sales_rep USING btree (sales_rep_key);
CREATE UNIQUE INDEX fact_bookings_pkey ON "QuoteToBooking".fact_bookings USING btree (booking_id);
```