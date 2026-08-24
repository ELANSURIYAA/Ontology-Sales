# Overall Validation Summary

| Metric | Score (%) |
|---------|-----------|
| Overall Validation Score | 82 |
| Accuracy Score | 84 |
| Efficiency Score | 81 |
| Completeness Score | 80 |
| Overall Status | PASS WITH WARNINGS |

# Completeness Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| Medium | Input Validation | Business domain context file `Inputs/Sales.txt` was not available, so glossary context remains inferred rather than validated against an authoritative business context document. | Provide the expected business domain context file and rerun validation to confirm business terminology and domain framing. |
| High | Object Coverage | The supplied OSI Semantic Model includes only the `quotetobooking` star-schema datasets and excludes `clarity.client` and `logging.combined_agent_details`, while the supplied data dictionary and metadata summary cover 10 tables across 3 schemas. | Confirm semantic model scope explicitly and either add the omitted tables with justified business purpose or formally exclude them from the governed model boundary. |
| Medium | Metadata Coverage | The semantic model does not carry nullability, source constraints, or profiling-based domain expectations present in the enriched metadata inputs. | Enrich the semantic model with constraint-oriented metadata where supported, or document that such metadata is intentionally maintained outside the semantic layer. |
| Medium | Documentation Coverage | Relationships are technically defined in the semantic model, but no relationship-level descriptions or business semantics are provided for the seven joins. | Add business descriptions for each relationship to improve governance clarity and downstream ontology interpretation. |
| High | Rule Coverage | The semantic model defines metrics but does not include explicit business rules or consistency constraints for `booking_type`, `is_renewal`, `discount_pct`, `acv_usd`, and `tcv_usd`. | Document governing business rules, value constraints, and derivation assumptions for measures and indicators used by downstream agents. |
| Medium | Mapping Coverage | Dataset-to-source table mapping is present, but explicit glossary-to-semantic mapping evidence for metrics and derived analytical concepts is not documented. | Add traceable mappings from glossary terms and business measures to semantic datasets, fields, and metric expressions. |

# Accuracy Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| Medium | Input Validation | The semantic model source was stated as output from the DI OSI Semantic Creator YAML Agent, but no separate file provenance or generation metadata was supplied for independent verification. | Include semantic model provenance metadata such as source artifact name, generation timestamp, and version lineage in future validations. |
| High | Object Scope Accuracy | The semantic model accurately represents the quote-to-booking star schema, but it does not represent the full supplied metadata estate of 10 tables, creating a scope mismatch against the broader input corpus. | Align validation scope between source metadata, glossary, and semantic model so the semantic artifact and its validation target the same in-scope objects. |
| Medium | Relationship Accuracy | The semantic model captures all seven declared fact-to-dimension relationships from the `quotetobooking` schema, but the underlying DDL uses unqualified referenced table names, which leaves schema-resolution ambiguity in the technical source. | Confirm physical foreign key resolution in PostgreSQL and document fully qualified source relationships in governed metadata. |
| Medium | Naming Convention Consistency | The semantic model omits the source column `aquiring_networks` because the corresponding table is out of scope, but the supplied glossary contains the misspelled physical attribute name, indicating a broader metadata naming inconsistency. | Normalize misspelled business aliases in governed metadata and preserve physical names only as technical source references. |
| Medium | Metric Accuracy | Metric expressions are technically valid, but several derived metrics such as `average_discount_pct`, `renewal_booking_amount_usd`, and `net_new_booking_amount_usd` rely on undocumented business assumptions about percentage representation and renewal coding. | Add authoritative business rule documentation for metric semantics and encoded field interpretations before downstream consumption. |
| Low | Business Definition Accuracy | Field descriptions in the semantic model are largely aligned with glossary definitions, but metric descriptions are not represented in the glossary as governed business terms, limiting cross-artifact verification depth. | Expand the glossary to include approved analytical metric definitions and validation rules for all published semantic metrics. |

# Efficiency Assessment

| Severity | Area | Issue | Recommendation |
|----------|------|-------|----------------|
| Medium | Structural Efficiency | The semantic model is efficiently focused on the analytical star schema and avoids unrelated operational tables, but the absence of an explicit scope statement may cause duplicate modeling efforts for excluded tables elsewhere. | Add a clear semantic scope declaration indicating that the model is intentionally limited to quote-to-booking analytics. |
| Low | Repeated Definitions | Dataset field descriptions closely repeat glossary definitions verbatim across dimensions and fact fields, which is consistent but creates maintenance duplication across artifacts. | Introduce shared metadata templates or lineage-driven synchronization to reduce repeated text across glossary and semantic model assets. |
| Medium | Duplicate Semantics | `booking_type` and `is_renewal` are both exposed in the semantic model and are both used to represent renewal meaning, which introduces semantic redundancy and possible downstream inconsistency. | Govern one attribute as primary and document the second as derived, constrained, or deprecated in semantic consumption layers. |
| Low | Optimization Opportunities | `average_booking_value_usd` divides by `COUNT(DISTINCT bookings.booking_id)` even though `booking_id` is the primary key of the fact dataset, making `DISTINCT` unnecessary under the current declared grain. | Simplify the metric to divide by `COUNT(bookings.booking_id)` if the booking grain remains guaranteed unique. |
| Low | Reusability | Common dimensional key patterns and repeated relationship structures are manually modeled across datasets without reusable semantic templates or conformance annotations. | Consider introducing reusable modeling conventions or generator templates for common dimension-key and relationship patterns. |