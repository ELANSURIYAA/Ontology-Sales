# Overall Validation Summary

| Metric | Score (%) |
|---------|-----------|
| Overall Validation Score | 85 |
| Accuracy Score | 92 |
| Efficiency Score | 81 |
| Completeness Score | 81 |
| Overall Status | PASS WITH WARNINGS |

# Completeness Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| Medium | Input Validation | Business domain context file `Ontology-Sales/Inputs/Sales.txt` was not accessible, so glossary provenance could not be validated against the cited source document. | Restore access to the business domain context file and revalidate glossary lineage against the authoritative source. |
| Medium | Relationship Coverage | The semantic model defines 7 fact-to-dimension relationships, but the relationships do not include business descriptions or semantic intent statements. | Add relationship descriptions documenting business meaning, filter propagation intent, and expected usage for each join. |
| Medium | Rule Coverage | The semantic model includes calculated metrics, but no explicit business rule documentation is provided for indicator/value semantics such as `is_renewal`, `discount_pct`, `acv_usd`, and `tcv_usd`. | Add formal business rules and calculation assumptions for indicators, percentages, and contract value measures. |
| Low | Mapping Coverage | Source-to-glossary alignment is implicitly strong through matching table and column names, but no explicit traceability identifiers or lineage metadata are included. | Add lineage or mapping identifiers linking glossary terms, semantic fields, and physical schema objects. |

# Accuracy Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| Medium | Business Definition Accuracy | Glossary business definitions were explicitly inferred because the domain context source file was unavailable, so business terminology cannot be confirmed as authoritative. | Reconcile inferred glossary definitions with approved business source documentation when available. |
| Medium | Technical Accuracy | The `bookings` dataset primary key is modeled as `booking_id`, while the AI context states the grain is booking transaction by booking identifier and order line; this introduces ambiguity because `order_line_number` is not part of the modeled primary key. | Confirm transactional grain and, if required by source semantics, document whether `booking_id` alone is sufficient or whether grain includes `order_line_number`. |
| Low | Naming Convention Consistency | Dataset naming is pluralized while source tables are singular/dimension-style names, which is acceptable but undocumented and may reduce semantic traceability for automated consumers. | Document dataset naming conventions and maintain a formal alias/mapping standard between semantic and physical object names. |
| Low | Duplicate Detection | `booking_type` and `is_renewal` both represent renewal semantics, creating potential interpretive overlap even though both map to valid source fields. | Document whether `is_renewal` is derived from `booking_type` or whether both attributes serve distinct analytical purposes. |

# Efficiency Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| Medium | Repeated Definitions | Foreign key field descriptions are repeated with nearly identical wording across the semantic model, which increases maintenance effort when terminology changes. | Use reusable description templates or inherited semantic patterns for common foreign key semantics. |
| Medium | Reusability | Multiple currency metrics (`total_booking_amount_usd`, `total_acv_usd`, `total_tcv_usd`, `renewal_booking_amount_usd`, `net_new_booking_amount_usd`, `average_booking_value_usd`) follow repeatable patterns but are not organized into reusable metric conventions. | Introduce shared metric design standards for additive currency measures, conditional measures, and average measures. |
| Low | Structural Efficiency | The model is structurally efficient and star-schema aligned, but field-level semantic typing is applied inconsistently because only some fields carry `dimension.is_time` metadata and measures lack analogous semantic typing metadata. | Standardize semantic annotations across dimensions, identifiers, attributes, and measures for better downstream automation. |
| Low | Optimization Opportunities | The semantic model is concise and well aligned to the source, but there are no explicit data quality constraints, enumerations, or reusable domains to support automated validation efficiency. | Add reusable domains, enumerations, and validation constraints for indicators, categories, and rate fields. |