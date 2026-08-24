# Overall Validation Summary

| Metric | Score (%) |
|---------|-----------|
| Overall Validation Score | 88 |
| Accuracy Score | 85 |
| Efficiency Score | 86 |
| Completeness Score | 93 |
| Overall Status | PASS WITH WARNINGS |

# Completeness Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| Medium | Attribute Coverage | The OKF bundle documents dataset-level attributes for all 8 entities, but it does not preserve source-level field metadata such as `dimension.is_time` flags from the OSI Semantic Model. | Add source-derived field-level metadata where applicable, especially semantic typing such as time indicators, to improve downstream machine validation. |
| Low | Metadata Coverage | The OKF bundle includes required YAML frontmatter on all reviewed files, but the bundle-level documentation does not explicitly carry forward the source `ai_context.instructions` outside the semantic summary. | Propagate source AI context or usage guidance into the primary bundle index or a dedicated governance note for stronger traceability. |
| Low | Mapping Coverage | Technical mappings are present for entity and relationship documents, but glossary terms are business-facing only and do not consistently indicate direct source provenance from the OSI model. | Add explicit provenance notes for glossary terms that are derived from source datasets, fields, or metrics. |

# Accuracy Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| High | Business Definition Accuracy | Several OKF documents introduce business rules and assertions not stated in the OSI Semantic Model, such as mandatory relationship requirements, immutability of bookings, dimension prepopulation requirements, and formula assertions for ACV/TCV. These go beyond the supplied source. | Restrict business rules and technical assertions to statements directly supported by the OSI Semantic Model, or clearly label them as derived assumptions if allowed by governance. |
| High | Mapping Accuracy | The bundle states that all booking relationships are mandatory and that each booking references exactly one record in each dimension. The OSI Semantic Model defines join structure but does not state nullability or mandatory referential constraints. | Remove mandatory/nullability claims unless they are explicitly present in source metadata. |
| Medium | Technical Accuracy | The relationship and entity documents infer star-schema implementation semantics and operational behavior, including referential integrity enforcement and dimension independence, that are not explicitly declared in the source YAML. | Keep structural descriptions aligned to the declared relationships only, without adding undeclared implementation guarantees. |
| Medium | Business Definition Accuracy | The glossary defines Net New Business as including customer expansion, while the source only identifies non-renewal via `is_renewal = 0` and does not specify expansion semantics. | Narrow the definition to non-renewal transactions unless the source model explicitly defines expansion logic. |
| Medium | Naming Convention Consistency | The source metric name is `average_discount_pct`, but the OKF file and title use “Average Discount Percentage” with file name `average-discount-pct.md`. This is readable but not a fully lossless preservation of source naming. | Include the exact source metric identifier in each measure document to ensure unambiguous traceability between OSI and OKF artifacts. |
| Low | Duplicate Detection | No direct duplicate entities, relationships, or measures were found, but several concepts are restated with expanded wording across summary, domain, glossary, and metric documents, increasing risk of future semantic drift. | Establish a canonical source statement per concept and reuse it consistently across derived documents. |

# Efficiency Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| Medium | Repeated Definitions | The bundle repeats long-form descriptions of the same entities, relationships, and measures across index, summary, domain, entity, relationship, and glossary documents. | Centralize canonical definitions and use shorter references in index-style documents to reduce maintenance overhead. |
| Medium | Unnecessary Complexity | Many documents contain extensive usage examples, derived metrics, and operational guidance that are not required to represent the source semantic model and may complicate downstream validation. | Limit documents intended for downstream automation to source-grounded semantics and move optional guidance to separate reference material if needed. |
| Low | Structural Efficiency | The bundle contains 50 OKF files for a source model with 1 domain, 8 datasets, 7 relationships, and 11 metrics. The navigation is complete, but the ratio of documentation volume to source complexity is high. | Consider a more compact OKF profile for smaller semantic models while preserving navigability and required metadata. |
| Low | Redundant Metadata | YAML frontmatter timestamps and common tags are repeated across nearly every file with limited differentiation value. | Standardize shared metadata centrally where possible and reserve file-level tags for concept-specific retrieval value. |

