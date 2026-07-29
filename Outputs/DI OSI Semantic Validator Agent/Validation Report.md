# Overall Validation Summary

| Metric | Score (%) |
|---------|-----------|
| Overall Validation Score | 82 |
| Accuracy Score | 84 |
| Efficiency Score | 79 |
| Completeness Score | 83 |
| Overall Status | PASS WITH WARNINGS |

# Completeness Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| Medium | Relationship Coverage | The OSI Semantic Model includes the seven technical relationships between dimensions and `quotetobooking.fact_bookings`, but the supplied business glossary does not provide relationship-level business definitions for those associations. | Add business definitions for each fact-to-dimension relationship so semantic intent is explicit in downstream knowledge engineering workflows. |
| Medium | Rule Coverage | The supplied artifacts do not document explicit business rules, derivation logic, or allowed values for important transactional and financial attributes such as `is_renewal`, `discount_pct`, `acv_usd`, and `tcv_usd`. | Add rule metadata and allowed-value guidance for indicators and financial measures to improve semantic completeness. |
| Medium | Documentation Coverage | The business domain context references booking analysis across product areas and booking types, but explicit controlled vocabulary documentation for fields such as `booking_type`, `offer_type`, `partner_type`, and `account_tier` is not fully formalized as governed value sets. | Add controlled vocabulary definitions and allowable values for categorical attributes used in analysis. |
| Low | Metadata Coverage | Technical nullability is present in the DDL and OSI Semantic Model, but the supplied glossary does not explicitly distinguish business-required fields from technically nullable fields in `quotetobooking.fact_bookings`. | Add business-requiredness metadata for nullable foreign keys and measures so downstream consumers can distinguish optionality from physical nullability. |
| Low | Input Validation | The supplied artifacts are readable and internally consistent, but provenance is presented as a combined package rather than as separately identified upstream deliverables from the semantic creator and glossary creator outputs. | Preserve separate source artifact identifiers or headers for upstream outputs to improve traceability in enterprise governance workflows. |

# Accuracy Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| High | Business Definition Accuracy | `discount_pct` is labeled as a percentage, but the profiled values range from `0.11` to `0.28`, which indicates fractional storage semantics rather than whole-number percentage values. | Clarify whether the attribute stores fractional rates or percentages and align its definition, naming, and usage guidance accordingly. |
| Medium | Business Definition Accuracy | The OSI Semantic Model defines `Date Key` as a surrogate key, but the observed values follow a meaningful `YYYYMMDD` date encoding pattern rather than an arbitrary surrogate identifier. | Revise the business definition to state that `date_key` is an integer-encoded date key if that is the intended design. |
| Medium | Naming Convention Consistency | `is_renewal` follows a boolean-style naming convention, but its physical type is `integer` and the artifacts do not explicitly document the code set beyond profiled values `0` and `1`. | Document the allowed coded values and their meanings, or adjust future naming standards to distinguish coded indicators from true booleans. |
| Medium | Technical Accuracy | `order_line_number` is defined as a line-level identifier, but profiling shows only one distinct value (`1`) across all fact rows, which limits evidence that the field behaves as a true order-line discriminator in the supplied dataset. | Confirm whether the sample dataset intentionally contains only single-line orders or whether the attribute is underrepresented relative to its stated meaning. |
| Low | Duplicate Detection | Several glossary mappings repeat highly similar key definitions across dimensions and fact references, which can create semantic ambiguity between a dimension surrogate key and a fact foreign key reference. | Differentiate master-key definitions from fact-reference definitions using a governed glossary pattern. |
| Low | Metadata Accuracy | The technical DDL expresses foreign key references with unqualified referenced table names, while the rest of the artifacts consistently use schema-qualified names such as `quotetobooking.dim_customer`. | Standardize metadata presentation so schema qualification is consistent across all technical artifacts. |

# Efficiency Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| Medium | Repeated Definitions | Many attribute definitions in the glossary and semantic model use repetitive phrasing patterns for surrogate keys, business identifiers, and fact references, increasing maintenance overhead. | Introduce standardized reusable definition templates for recurring semantic patterns. |
| Medium | Redundant Metadata | The supplied technical metadata includes both primary key constraints and matching unique indexes for the same columns across all tables, which is useful technically but redundant for semantic governance outputs. | Suppress or consolidate duplicate key/index metadata in downstream semantic documentation unless index details are specifically required. |
| Medium | Structural Efficiency | The validation input combines schema, profiling, glossary, and semantic model content into one large package, which reduces traceability and makes issue isolation less efficient. | Maintain separate but linked artifacts for schema discovery, profiling, glossary, and semantic model outputs with consistent identifiers. |
| Low | Unnecessary Complexity | `booking_type` and `is_renewal` partially overlap semantically for the observed values `New` and `Renewal`, creating potential duplication in downstream semantic consumption. | Document the distinct business purpose of each attribute and whether one is derived from the other. |
| Low | Optimization Opportunities | Several low-cardinality descriptive attributes such as `segment`, `account_tier`, `offer_type`, and `booking_type` could support stronger semantic reuse if governed as shared controlled vocabularies. | Establish controlled vocabularies and reusable reference standards for low-cardinality business classifications. |
| Low | Reusability | Business categories are applied consistently, but the supplied artifacts do not include an enterprise taxonomy or synonym standard that would improve reuse across adjacent sales and finance domains. | Add taxonomy and synonym governance for domains, entities, and measures to improve cross-domain semantic reuse. |