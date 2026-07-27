# Ontology Validation Report

## Validation Summary

| Metric | Score | Reason |
|--------|------:|--------|
| Overall Validation Score | 99% | The Turtle ontology is an almost lossless, semantically faithful serialization of the OWL ontology with only negligible representation differences. |
| Completeness | 100% | All ontology elements (ontology header, prefixes, classes, restrictions, object and datatype properties, annotation properties, and disjointness axioms) from the OWL source are present in the Turtle ontology. |
| Accuracy | 98% | Semantics of domains, ranges, cardinalities, inverses, and annotations are preserved; only minor syntactic representation changes (e.g., explicit typing of functional properties) are observed but remain logically equivalent. |
| Efficiency | 98% | The Turtle file is concise, uses shared blank nodes for restrictions and disjointness, and avoids redundancy; minor opportunities exist for further normalization but do not affect performance. |

## Completeness Findings

| Severity | Area | Issue Identified | Recommendation |
|----------|------|------------------|----------------|
| None | N/A | No missing classes, properties, restrictions, or annotations were found compared to the OWL ontology. | No action required. |

## Accuracy Findings

| Severity | Area | Issue Identified | Recommendation |
|----------|------|------------------|----------------|
| Low | Object Properties | Functional object properties (e.g., `hasContract`, `hasCustomer`, `hasBookingDate`, etc.) are represented in Turtle as both `owl:ObjectProperty` and `owl:FunctionalProperty` types, whereas the OWL source used a dedicated `rdf:type owl:FunctionalProperty` triple. This is semantically equivalent but changes the syntactic pattern. | Accept as-is, as the semantics are preserved. If strict structural parity is required by downstream tooling, document this pattern in the converter’s specification to avoid false positives in future validations. |
| Low | Datatype Properties | Datatype keys (e.g., `customerId`, `productId`, `partnerId`, `salesRepKey`, etc.) are explicitly typed as both `owl:DatatypeProperty` and `owl:FunctionalProperty` in Turtle, matching but slightly refactoring the original RDF/XML representation. | No change needed. Maintain this explicit dual typing as a best practice and ensure tests understand this representation as equivalent. |
| Low | Anonymous Axioms | The `owl:AllDisjointClasses` axiom is represented using a blank node and an RDF list of class IRIs in Turtle, instead of the RDF/XML `rdf:parseType="Collection"` form. This is behaviorally identical but structurally different. | No action required. Note this as the expected canonical Turtle pattern and ensure comparison tooling accounts for list-based encodings of collections. |
| Low | Restrictions | All `owl:Restriction` axioms on `BookingTransaction` (max qualified cardinality of 1 for each dimension) are preserved as anonymous restrictions with `owl:maxQualifiedCardinality`, `owl:onClass`, and `owl:onProperty` in Turtle. Minor serialization ordering differences exist but do not affect semantics. | No change needed. If automated diffing is used, rely on graph-level rather than textual/ordering comparisons to avoid spurious mismatches. |

## Efficiency Findings

| Severity | Area | Issue Identified | Recommendation |
|----------|------|------------------|----------------|
| Low | Structural Redundancy | Object and datatype properties that are functional are declared once and typed with both `owl:ObjectProperty`/`owl:DatatypeProperty` and `owl:FunctionalProperty`. This is semantically desirable but adds one extra triple per functional property. | Keep the current explicit typing for clarity and standards compliance. If file size optimization becomes critical, consider documenting an optional profile that omits `owl:FunctionalProperty` where max-cardinality restrictions already constrain functionality. |
| Low | Use of Blank Nodes | Restrictions and the `owl:AllDisjointClasses` axiom are encoded using blank nodes, which is efficient and idiomatic in Turtle but can be less directly referencable for some tooling. | Retain blank-node usage, as it reduces IRI proliferation and keeps the TTL compact. If some tools require named axioms, consider an optional transformation step outside the core converter. |
