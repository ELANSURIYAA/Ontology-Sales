# Overall Validation Summary

| Metric | Score (%) |
|---------|-----------|
| Overall Validation Score | 66 |
| Accuracy Score | 72 |
| Efficiency Score | 70 |
| Completeness Score | 55 |
| Overall Status | PASS WITH WARNINGS |

# Completeness Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| Medium | Input Validation | Business domain context file `Inputs/Sales.txt` was not available, so glossary context is incomplete and inferred rather than sourced from the expected business input. | Provide the expected business domain context file and rerun validation to confirm glossary terms and definitions against authoritative business documentation. |
| High | Business Glossary Coverage | No source business glossary artifact from a dedicated glossary steward source was supplied; business terms and definitions are derived from schema and profiling outputs only. | Supply the original enriched glossary artifact from the DI Glossary Creator Agent with authoritative business-approved terminology and definitions. |
| High | Documentation Coverage | Relationship-level business definitions are absent for the seven foreign key associations in the quote-to-booking model. | Add business descriptions for each relationship so downstream semantic modeling can distinguish lookup, conformance, and analytical join intent. |
| High | Rule Coverage | No documented business rules, derivation rules, or validation constraints were supplied for measures such as `booking_amount_usd`, `acv_usd`, `tcv_usd`, `discount_pct`, and `is_renewal`. | Add calculation logic, semantic constraints, and allowed-value rules for transactional measures and indicators. |
| Medium | Mapping Coverage | No source-to-target mappings, lineage mappings, or term-to-column mapping evidence were supplied beyond direct column descriptions. | Provide explicit business-to-technical mappings and lineage references for glossary stewardship and ontology generation traceability. |
| Medium | Object Coverage | The dataset includes 10 tables across 3 schemas, but only the `quotetobooking` schema forms a coherent analytical star model; `clarity.client` and `logging.combined_agent_details` are not connected by declared relationships or contextual mapping. | Document whether these tables are in scope for the semantic model and define their business integration points or exclude them formally. |
| Medium | Attribute Documentation | Columns with encoded or domain-specific semantics such as `arb`, `aims_id`, `ig_league_name`, `vau_segment_id`, and `current_pseudorouting` have only generic inferred definitions without authoritative domain expansion. | Enrich these columns with steward-approved definitions, source-system references, and valid domain descriptions. |
| Medium | Domain Assignment | Business categories are present but there is no enterprise domain taxonomy or controlled vocabulary showing that categories like `Sales Dimension`, `Product Master`, and `Revenue Metrics` conform to approved domains. | Align glossary categories to an approved enterprise domain model and controlled list of subject areas. |

# Accuracy Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
|----------|------|-------|----------------|
| High | Business Definition Accuracy | The glossary explicitly states that business domain context was inferred because `Inputs/Sales.txt` was unavailable, so all business definitions lack verification against authoritative business source material. | Validate all table and column definitions with business owners before using them for ontology or semantic model generation. |
| High | Relationship Accuracy | DDL foreign key statements reference dimension tables without schema qualification (`REFERENCES dim_contract(contract_key)` etc.), while relationship summaries use fully qualified names; this creates ambiguity in multi-schema environments. | Confirm actual foreign key resolution in PostgreSQL and document all relationships with fully qualified schema names. |
| Medium | Naming Convention Consistency | Column name `aquiring_networks` appears to be a misspelling of `acquiring_networks`, creating inconsistency between technical naming and business terminology. | Confirm whether the physical column name is intentional; if retained physically, document the correct business term and add an alias for semantic modeling. |
| Medium | Metadata Accuracy | `discount_pct` is profiled with values from `0.11` to `0.28`, while the glossary defines it as a percentage without clarifying whether the stored representation is fractional or whole-percent. | Clarify the representation standard for percentage fields and document whether values are decimals, percentages, or normalized ratios. |
| Medium | Business Definition Accuracy | `arb` is defined generically as `Revenue-related metric associated with the client account`, which is too vague to accurately capture the intended business meaning of the acronym. | Expand the acronym with authoritative source meaning and document formula, unit, and business usage. |
| Medium | Technical Accuracy | `is_renewal` is defined as an indicator but implemented as integer rather than boolean/flag domain, with no documented allowable values beyond profile observations. | Document the valid value set and semantic interpretation for integer indicator fields. |
| Medium | Business Definition Accuracy | `coverage_level` includes values such as `EA`, `Expert`, `None`, `24x7`, and `24x7x4`, which appear to mix support levels, service styles, and abbreviations under a single attribute. | Confirm whether these values belong to one domain and define standardized permissible values with business meaning. |
| Medium | Duplicate Detection | `booking_type` and `is_renewal` encode overlapping renewal semantics, increasing risk of contradictory values if not constrained. | Define a consistency rule between the two attributes or consolidate to a single governed business concept in downstream semantic layers. |
| Low | Naming Convention Consistency | Business categories vary in style and granularity, for example `Sales Dimension`, `Customer Master`, `Pricing`, and `Organizational Alignment`, which may reduce consistency in downstream semantic grouping. | Standardize category naming depth and classification rules across all glossary entries. |

# Efficiency Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| Medium | Redundant Metadata | The glossary repeats common surrogate-key definitions such as `Surrogate key that uniquely identifies...` across dimension tables with minimal specialization. | Introduce reusable metadata patterns or templates for common key concepts to reduce duplication in governed glossary maintenance. |
| Medium | Repeated Definitions | Multiple foreign key columns in `fact_bookings` are documented using nearly identical `Reference to the ... dimension` phrasing, which is semantically correct but repetitive. | Use standardized reusable relationship templates while preserving explicit target-dimension references. |
| Medium | Duplicate Documentation | `booking_type` and `is_renewal` document the same renewal concept twice at the glossary level, mirroring semantic redundancy in the model. | Rationalize overlapping business concepts and define one as derived, dependent, or deprecated for downstream modeling. |
| Medium | Structural Efficiency | `clarity.client` and `logging.combined_agent_details` are structurally isolated from the quote-to-booking star schema, reducing semantic cohesion if all tables are modeled together. | Partition the glossary into bounded business domains or explicitly separate analytical, operational, and logging subject areas. |
| Low | Unnecessary Complexity | `logging.combined_agent_details.diagnostic_logs` stores verbose JSONB diagnostic narratives that are unlikely to contribute to enterprise business glossary use cases. | Consider limiting glossary emphasis for highly technical audit attributes or classifying them under a technical metadata subdomain. |
| Low | Optimization Opportunities | `order_line_number` has a single observed value of `1` across all profiled rows, suggesting either underutilized granularity or a sample not exercising line-level detail. | Verify whether line-level granularity is required and document expected future variability or simplify semantic exposure if not needed. |
| Low | Reusability | Geographic concepts appear in both `clarity.client` (`city`, `state_name`, `zip`) and `quotetobooking.dim_geography` (`region`, `theater`, `country`) without a shared governed geography vocabulary. | Establish reusable conformed geography terminology and domain standards across subject areas. |