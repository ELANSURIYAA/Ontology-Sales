# Metadata Summary

| Metric | Value |
| --- | --- |
| Database Type | PostgreSQL |
| Number of Schemas | 3 |
| Number of Tables | 10 |
| Number of Columns | 101 |
| Number of Primary Keys | 9 |
| Number of Foreign Keys | 7 |
| Number of Views | 0 |
| Number of Procedures/Functions | 0 |
| Number of Triggers | 0 |
| Number of Sequences | 1 |

## Relationships

| Parent Table | Child Table | Referenced Columns | Relationship Type |
| --- | --- | --- | --- |
| quotetobooking.dim_contract | quotetobooking.fact_bookings | contract_key | One-to-Many |
| quotetobooking.dim_customer | quotetobooking.fact_bookings | customer_key | One-to-Many |
| quotetobooking.dim_date | quotetobooking.fact_bookings | date_key | One-to-Many |
| quotetobooking.dim_geography | quotetobooking.fact_bookings | geography_key | One-to-Many |
| quotetobooking.dim_partner | quotetobooking.fact_bookings | partner_key | One-to-Many |
| quotetobooking.dim_product | quotetobooking.fact_bookings | product_key | One-to-Many |
| quotetobooking.dim_sales_rep | quotetobooking.fact_bookings | sales_rep_key | One-to-Many |

## DDL Definitions

```sql
CREATE TABLE clarity.client (
  client_id bigint,
  migration_date date,
  financial_institution_name character varying(255),
  entity_id bigint,
  cardcount integer,
  vru_activation_options character varying(255),
  fi_id bigint,
  aims_id bigint,
  ig_league_name character varying(255),
  arb numeric(15,2),
  routing_id character varying(50),
  city character varying(100),
  state_name character varying(100),
  fi_primary_contact_name character varying(255),
  fi_primary_contact_phone character varying(50),
  fraudcontactgroup_email character varying(255),
  address character varying(500),
  zip character varying(20),
  fi_primary_contact_email character varying(255),
  current_pseudorouting character varying(50),
  issuing_networks character varying(255),
  aquiring_networks character varying(255),
  vau_segment_id bigint,
  migration_wave integer
);

CREATE TABLE logging.combined_agent_details (
  id bigint NOT NULL DEFAULT nextval('logging.combined_agent_details_id_seq'::regclass),
  project_key character varying(50),
  ticket_key character varying(100),
  ticket_id character varying(100),
  ticket_url text,
  github_owner character varying(255),
  github_repository character varying(255),
  github_branch character varying(255),
  github_file_path text,
  attachment_id character varying(100),
  attachment_name text,
  attachment_status character varying(50),
  status character varying(50),
  error_message text,
  diagnostic_logs jsonb,
  created_at timestamp without time zone DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE quotetobooking.dim_contract (
  contract_key integer NOT NULL,
  contract_type character varying(40),
  term_months integer,
  auto_renew_flag character(1),
  coverage_level character varying(20)
);

CREATE TABLE quotetobooking.dim_customer (
  customer_key integer NOT NULL,
  customer_id character varying(20) NOT NULL,
  customer_name character varying(80),
  segment character varying(30),
  industry character varying(40),
  account_tier character varying(20),
  hq_country character varying(40),
  hq_region character varying(20)
);

CREATE TABLE quotetobooking.dim_date (
  date_key integer NOT NULL,
  full_date date NOT NULL,
  month_name character varying(12),
  calendar_year integer,
  fiscal_year character varying(6),
  fiscal_quarter character varying(10),
  fiscal_period_seq integer
);

CREATE TABLE quotetobooking.dim_geography (
  geography_key integer NOT NULL,
  region character varying(20),
  theater character varying(30),
  country character varying(40)
);

CREATE TABLE quotetobooking.dim_partner (
  partner_key integer NOT NULL,
  partner_id character varying(20) NOT NULL,
  partner_name character varying(60),
  partner_type character varying(30),
  partner_tier character varying(30),
  route_to_market character varying(20)
);

CREATE TABLE quotetobooking.dim_product (
  product_key integer NOT NULL,
  product_id character varying(30) NOT NULL,
  product_name character varying(80),
  product_family character varying(30),
  technology_domain character varying(40),
  offer_type character varying(30),
  business_entity character varying(30)
);

CREATE TABLE quotetobooking.dim_sales_rep (
  sales_rep_key integer NOT NULL,
  rep_id character varying(20) NOT NULL,
  rep_name character varying(60),
  sales_role character varying(40),
  sales_team character varying(40),
  segment_covered character varying(30)
);

CREATE TABLE quotetobooking.fact_bookings (
  booking_id integer NOT NULL,
  order_number character varying(20),
  order_line_number integer,
  date_key integer,
  customer_key integer,
  product_key integer,
  partner_key integer,
  geography_key integer,
  sales_rep_key integer,
  contract_key integer,
  booking_type character varying(15),
  is_renewal integer,
  quantity integer,
  unit_list_price_usd numeric(12,2),
  discount_pct numeric(5,2),
  booking_amount_usd numeric(14,2),
  acv_usd numeric(14,2),
  tcv_usd numeric(14,2)
);

ALTER TABLE logging.combined_agent_details ADD PRIMARY KEY (id);
ALTER TABLE quotetobooking.dim_contract ADD PRIMARY KEY (contract_key);
ALTER TABLE quotetobooking.dim_customer ADD PRIMARY KEY (customer_key);
ALTER TABLE quotetobooking.dim_date ADD PRIMARY KEY (date_key);
ALTER TABLE quotetobooking.dim_geography ADD PRIMARY KEY (geography_key);
ALTER TABLE quotetobooking.dim_partner ADD PRIMARY KEY (partner_key);
ALTER TABLE quotetobooking.dim_product ADD PRIMARY KEY (product_key);
ALTER TABLE quotetobooking.dim_sales_rep ADD PRIMARY KEY (sales_rep_key);
ALTER TABLE quotetobooking.fact_bookings ADD PRIMARY KEY (booking_id);
ALTER TABLE quotetobooking.fact_bookings ADD FOREIGN KEY (contract_key) REFERENCES dim_contract(contract_key);
ALTER TABLE quotetobooking.fact_bookings ADD FOREIGN KEY (customer_key) REFERENCES dim_customer(customer_key);
ALTER TABLE quotetobooking.fact_bookings ADD FOREIGN KEY (date_key) REFERENCES dim_date(date_key);
ALTER TABLE quotetobooking.fact_bookings ADD FOREIGN KEY (geography_key) REFERENCES dim_geography(geography_key);
ALTER TABLE quotetobooking.fact_bookings ADD FOREIGN KEY (partner_key) REFERENCES dim_partner(partner_key);
ALTER TABLE quotetobooking.fact_bookings ADD FOREIGN KEY (product_key) REFERENCES dim_product(product_key);
ALTER TABLE quotetobooking.fact_bookings ADD FOREIGN KEY (sales_rep_key) REFERENCES dim_sales_rep(sales_rep_key);

CREATE UNIQUE INDEX combined_agent_details_pkey ON logging.combined_agent_details USING btree (id);
CREATE UNIQUE INDEX dim_contract_pkey ON quotetobooking.dim_contract USING btree (contract_key);
CREATE UNIQUE INDEX dim_customer_pkey ON quotetobooking.dim_customer USING btree (customer_key);
CREATE UNIQUE INDEX dim_date_pkey ON quotetobooking.dim_date USING btree (date_key);
CREATE UNIQUE INDEX dim_geography_pkey ON quotetobooking.dim_geography USING btree (geography_key);
CREATE UNIQUE INDEX dim_partner_pkey ON quotetobooking.dim_partner USING btree (partner_key);
CREATE UNIQUE INDEX dim_product_pkey ON quotetobooking.dim_product USING btree (product_key);
CREATE UNIQUE INDEX dim_sales_rep_pkey ON quotetobooking.dim_sales_rep USING btree (sales_rep_key);
CREATE UNIQUE INDEX fact_bookings_pkey ON quotetobooking.fact_bookings USING btree (booking_id);

CREATE SEQUENCE logging.combined_agent_details_id_seq;
```